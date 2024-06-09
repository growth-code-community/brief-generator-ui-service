<template>
  <div class="brief">
    <div class="top">
      <p>Logo Brief</p>
      <button class="white">
        Export Brief
        <img src="@/assets/icons/export.svg" alt="" />
      </button>
    </div>
    <div class="container mt-3">
      <p>
        <b>Company Name:</b> <br />
        Up Branch
      </p>

      <p>
        <b>Company Description:</b>
        We are a company that makes and distributes Mexican soft drinks. Our
        main product is made with a secret recipe and available in stores
        worldwide. Our target audience is parents. We want to convey a sense of
        delight, while at the same time being modern.
      </p>

      <p>
        <b>Job Description:</b>
        You must create a website that will mainly provide customer support for
        the company. The goal is to emphasize the brand's values. Besides the
        landing page, the website will need a about page, product pages and a
        privacy policy page. The landing page should have a Contact Us section.
        There should be a call to action to get users to follow the company's
        social media. They would prefer a old-fashioned design, and would like
        you to use the brand color, which is white. Take into account the
        client's preferences and values.
      </p>

      <p>
        <b>Deadline:</b>
        2 days
      </p>
    </div>

    <div class="profile mt-3">
      <img src="@/assets/images/profile.png" alt="" />
      <div class="content">
        <p class="font-size-10">Good Brief</p>
        <p class="font-size-12"><b>Growth Team</b></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
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
