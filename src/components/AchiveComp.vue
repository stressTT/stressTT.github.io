<template>
  <div class="Achive flex">
    <div>
      <p>4</p>
      <span
        >офиса в Астане <br />
        и области</span
      >
    </div>

    <div>
      <p>15</p>
      <span
        >лет практики <br />
        на рынке</span
      >
    </div>

    <div>
      <p>300</p>
      <span>сотрудников <br />в штате</span>
    </div>

    <div>
      <p>250</p>
      <span
        >надежных <br />
        партнеров</span
      >
    </div>
  </div>
</template>

<style lang="less" scoped>
.Achive {
  background: #fff;
  padding: 0 3%;
  div {
    text-align: center;
    padding: 5% 3.6%;
    border-right: 1px solid rgba(0, 0, 0, 0.1);
    width: 25%;
    p {
      font-size: 60px;
      color: rgba(var(--main-2), 1);
    }
    span {
      font-size: 19px;
    }
  }
  div:last-child {
    border: none;
  }
}
@media (max-width: 479px) {
  .Achive {
    padding: 0 0 20px; //e
    display: flex; //e
    flex-wrap: wrap; //e
    div {
      text-align: start; //e
      padding: 20px; //e
      border-right: 1px solid rgba(0, 0, 0, 0); //e
      width: 100%; //e
      display: flex; //e
      align-items: center; //e
      flex-wrap: wrap; //e
      p {
        font-size: 39px; //e
        border-right: 1px solid rgba(0, 0, 0, 0); //e
        padding: 5px 0; //e
        margin-right: 20px; //e
      }
      span {
        font-size: 18px; //e
      }
    }
  }
}
@media (min-width: 480px) and (max-width: 767px) {
  .Achive {
    padding: 0 0 20px; //e
    display: flex; //e
    flex-wrap: wrap; //e
    div {
      text-align: start; //e
      padding: 25px; //e
      border-right: 1px solid rgba(0, 0, 0, 0); //e
      width: 50%; //e
      display: flex; //e
      align-items: center; //e
      flex-wrap: wrap; //e
      p {
        font-size: 39px; //e
        border-right: 1px solid rgba(0, 0, 0, 0); //e
        padding: 5px 20px 5px 0; //e
        margin-right: 20px; //e
      }
      span {
        font-size: 18px; //e
      }
    }
  }
}
@media (min-width: 768px) and (max-width: 1023px) {
  .Achive {
    padding: 20px 5px; //e
    display: flex; //e
    flex-wrap: wrap; //e
    div {
      text-align: start; //e
      padding: 25px 30px; //e
      border-right: 1px solid rgba(0, 0, 0, 0); //e
      width: 50%; //e
      display: flex; //e
      align-items: center; //e
      p {
        font-size: 45px; //e
        border-right: 1px solid rgba(0, 0, 0, 0.1); //e
        padding: 5px 20px 5px 0; //e
        margin-right: 20px; //e
      }
      span {
        font-size: 18px; //e
      }
    }
  }
} ;
</style>
