<template>
    <div class="hero">
        <Banner />
        <div class="container mt-3">
            <div>
                <form @submit.prevent="generateBrief">
                    <div class="top">
                        <p class="weight-5 mb-1">Create Brief</p>
                    </div>

                    <div class="container mt-2">
                        <div class="content">
                            <p>Type</p>
                            <select name="" id="">
                                <option value="">Logo</option>
                            </select>
                        </div>

                        <div class="content">
                            <p>Industry</p>
                            <select name="" id="">
                                <option value="">Technology</option>
                            </select>
                        </div>
                    </div>

                    <div class="prompt mt-2">
                        <textarea name="" id=""
                            placeholder="Result should be focused on making logo better to improve customer retention"></textarea>
                    </div>

                    <button class="mt-3 mb-3 p-1">
                        Generate AI Brief&nbsp; <img src="../assets/images/mdi_send.png" alt="" />
                    </button>
                </form>
            </div>
            <div>
                <div class="brief">
                    <div class="top">
                        <p>Logo Brief</p>
                        <button class="white">
                            Export Brief
                            <img src="@/assets/icons/export.svg" alt="" />
                        </button>
                    </div>
                    <div class="container mt-3">
                        <div v-html="geminiResponse"></div>
                    </div>

                    <div class="profile mt-3">
                        <img src="@/assets/images/profile.png" alt="" />
                        <div class="content">
                            <p class="font-size-10">Good Brief</p>
                            <p class="font-size-12"><b>Growth Team</b></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

import Banner from './Banner'
import Form from './Form'
import Brief from './Brief.vue';

export default {
    data() {
        return {
            geminiResponse : null
        }
    },
    components: {
        Banner,
        Form,
        Brief
    },
    methods: {
    generateBrief() {
      let data = JSON.stringify({
        "type": "logo",
        "industry": "finance",
        "custom_prompt": ""
      });

      let config = {
        method: 'post',
        maxBodyLength: Infinity,
        url: 'http://localhost:3001/generate-brief',
        headers: {
          'Content-Type': 'application/json'
        },
        data: data
      };
      
      let self = this

      axios.request(config)
        .then((response) => {
          console.log(JSON.stringify(response.data.data.geminiResponse));
            self.geminiResponse  = response.data.data.geminiResponse
        })
        .catch((error) => {
          console.log(error);
        });

    }
  }
}
</script>

<style scoped>
.hero {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 150px 120px 0px;
    padding: 0px;

    max-width: 1500px;

    @media (width < 1000px) {
        margin: 150px 40px 0px;
    }

    @media (width < 700px) {
        margin: 90px 20px;
    }
}

.container {
    display: grid;
    grid-template-columns: 2fr 3fr;
    /* Replace percentages with fr units */
    gap: 20px;
    margin-bottom: 50px;
    width: inherit;

    @media (width < 1000px) {
        margin-top: 20px;
        grid-template-columns: 1fr;
    }
}



/* form */

form {
  background-color: #fafafa1a;
  display: flex;
  flex-direction: column;
  align-items: stretch;
  padding: 32px;
  border-radius: 8px;

  @media (width < 700px) {
    padding: 16px;
  }
}

form .top {
  display: flex;
  flex-direction: column;
  gap: 8px;
  border-bottom: 0.5px solid #ffffff7f;
}

form .container {
  display: flex;
  align-items: center;
  gap: 24px;
  align-items: stretch;
  width: 100%;
}

form .container .content {
  display: flex;
  flex-direction: column;
  gap: 12px;
  align-items: stretch;
  width: 100%;
}

form .container .content select {
  display: flex;
  padding: 8px;
  background: url(@/assets/icons/dropdown_arrow.svg) 95% center no-repeat #ffffff5c !important;
  border-radius: 4px;
  color: #ffffff;
  font-size: 16px;
  font-weight: 500;
  width: 100%;
  -webkit-appearance: none;
  outline: none;
}

form .prompt {
  display: flex;
  flex-direction: column;
  gap: 12px;
  align-items: stretch;
  height: 200px;
}

form .prompt textarea {
  background-color: #ffffff5c;
  color: #ffffff;
  height: 100%;
  padding: 10px;
  font-size: 16px;
  font-weight: 500;
  border-radius: 4px;
  outline: 0px;
}

textarea::placeholder {
  color: #ffffff;
}

button {
  background-color: #ffffff;
  font-weight: 700;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  border-radius: 100px;

}

/* brief */

.brief {
  background-color: #fafafa1a;
  display: flex;
  flex-direction: column;
  align-items: stretch;
  padding: 32px;
  border-radius: 8px;
  width: 100%;

  @media (width < 700px) {
    padding: 16px;
  }
}

.brief .top {
  display: flex;
  justify-content: space-between;
}

.brief .top button {
  background-color: black;
  display: flex;
  align-items: center;
  gap: 5px;
  border-radius: 100px;
  padding: 7px 12px;
  border: 0px;
}

.brief .container {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  gap: 32px;
}

.brief .container p {
  font-weight: 300 !important;
  line-height: 25px;
}

.brief .profile {
  display: flex;
  gap: 5px;
  align-items: center;
}

.brief .profile .content {
  display: flex;
  flex-direction: column;
  gap: 5px;
  @media (width < 900px) {
  }
}
</style>