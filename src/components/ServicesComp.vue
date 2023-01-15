<template>
  <div class="services">
    <div class="nav">
      <span>Виды услуг</span>
      <h1>Предлагаем организацию практически любых перевозок по всему миру</h1>
    </div>
    <div class="main">
      <div class="service">
        <p>Автомобильные</p>
        <span>перевозоки</span>
      </div>
      <div class="service">
        <p>Железнодорожные</p>
        <span>перевозоки</span>
      </div>
      <div class="service">
        <p>Авиа</p>
        <span>перевозоки</span>
      </div>
      <div class="consultant">
        <div class="name">
          <img src="../assets/img/фыв1.jpg" alt="" />
          <div>
            <p>Zhxns Beatmaker</p>
            <span>Консультант</span>
          </div>
        </div>
        <div class="num">
          <span class="numbers" href="">+7 700 000 0000</span>
          <button class="btnPrice">
            Отправить
            <i class="fa-solid fa-caret-right iconPrice"></i>
          </button>
        </div>
      </div>
      <div class="foot">
        <span
          >Оказываем профессиональные услуги, которые помогают вашему бизнесу
          функционировать. Работаем с отдельными компаниями, группами и
          холдингами в Астане, Акмолинской области и по всему Казахстану.</span
        >
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.services {
  padding-top: 7%;
  padding-bottom: 2%;
  position: relative;
  z-index: 0;

  .nav {
    padding: 0 7% 3.8%;
    color: #fff;
    text-align: center;
    width: 100%;
    display: block;

    span {
      font-size: clamp(28px, 33.5vw, 80px);
      line-height: normal;
    }
    h1 {
      opacity: 0.5;
      font-size: 20px;

      letter-spacing: 0.3px;
      font-weight: 400;
      line-height: 27px;
      max-width: 500px;
      margin: 10px auto 0;
    }
  }
  .main {
    width: 100%;
    padding: 0 7%;

    .service {
      cursor: pointer;
      padding: 6%;
      width: 100%;
      background: #fff;
      color: #121212;
      border-bottom: 1px solid rgba(0, 0, 0, 0.1);
      transition: 0.2s all;
      p {
        font-size: clamp(23px, 2.7vw, 45px);
        transition: 0.5s all;
      }
      span {
        font-size: 20px;
        letter-spacing: 0.3px;
        width: 100%;
        transition: 0.5s all;
      }
      &:hover {
        p {
          margin-left: 10px;
        }
        span {
          margin-left: 10px;
        }
        background: rgb(241, 241, 241);
      }
    }
    .consultant {
      width: 100%;
      background: rgba(var(--main-1));
      padding: 45px 50px;
      display: flex;
      align-items: center;
      color: rgba(var(--white));
      justify-content: space-between;

      .name {
        display: flex;
        align-items: center;
        width: 50%;
        img {
          width: 140px;
          height: 140px;
          object-fit: cover;
          border: 10px solid rgba(var(--white), 0.15);
          border-radius: 50%;
          margin-right: 20px;
        }
        p {
          font-size: 23px;
          letter-spacing: 0.3px;
        }
        span {
          font-size: 19px;
          letter-spacing: 0.3px;
          opacity: 0.7;
        }
      }
      .num {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 50%;
        padding-left: 30px;
        flex-wrap: wrap;
        span {
          font-size: 26px;
          font-weight: 400;
          cursor: pointer;
          padding: 15px 0;
        }
        .btnPrice {
          background: rgba(var(--main-2));
          border: 2px solid rgba(var(--main-2));
          i {
            color: rgba(var(--main-2));
          }
          &:hover {
            color: rgba(var(--main-2));
            i {
              background: rgba(var(--main-2));
              color: rgba(var(--white));
            }
          }
        }
      }
    }
    .foot {
      padding: 50px 60px;
      text-align: center;
      font-size: 18px;
      color: rgba(var(--white), 0.5);
      line-height: 27px;
      width: 100%;
      letter-spacing: 0.3px;
      span {
        flex-grow: 1;
      }
    }
  }
}
@media (max-width: 480px) {
}
@media (min-width: 480px) and (max-width: 767px) {
}
@media (min-width: 768px) and (max-width: 1023px) {
  .services {
    padding-top: 0; // e
    padding-bottom: 0; //e
    position: relative;
    z-index: 0;

    .nav {
      padding: 40px 30px;
      color: #fff;
      text-align: start;
      width: 100%;
      display: block;

      span {
        font-size: 3.5vw;
        line-height: normal;
      }
      h1 {
        opacity: 0.5;
        font-size: 19px; //e

        letter-spacing: 0.3px;
        font-weight: 400;
        line-height: 25px; //e
        max-width: 500px;
        margin: 10px 0 0; //e
      }
    }
    .main {
      width: 100%;
      padding: 0; //e

      .service {
        cursor: pointer;
        padding: 40px 30px; //e
        width: 100%;
        background: #fff;
        color: #121212;
        border-bottom: 1px solid rgba(0, 0, 0, 0.1);
        transition: 0.2s all;
        p {
          transition: 0.5s all;
        }
        span {
          font-size: 20px;
          letter-spacing: 0.3px;
          width: 100%;
          transition: 0.5s all;
        }
        &:hover {
          p {
            margin-left: 10px;
          }
          span {
            margin-left: 10px;
          }
          background: rgb(241, 241, 241);
        }
      }
      .consultant {
        width: 100%;
        background: rgba(var(--main-1));
        padding: 45px 50px;
        display: flex;
        align-items: center;
        color: rgba(var(--white));
        justify-content: space-between;

        .name {
          display: flex;
          align-items: center;
          width: 50%;
          img {
            width: 140px;
            height: 140px;
            object-fit: cover;
            border: 10px solid rgba(var(--white), 0.15);
            border-radius: 50%;
            margin-right: 20px;
          }
          p {
            font-size: 23px;
            letter-spacing: 0.3px;
          }
          span {
            font-size: 19px;
            letter-spacing: 0.3px;
            opacity: 0.7;
          }
        }
        .num {
          display: flex;
          justify-content: space-between;
          align-items: center;
          width: 50%;
          padding-left: 30px;
          flex-wrap: wrap;
          span {
            font-size: 26px;
            font-weight: 400;
            cursor: pointer;
            padding: 15px 0;
          }
          .btnPrice {
            background: rgba(var(--main-2));
            border: 2px solid rgba(var(--main-2));
            i {
              color: rgba(var(--main-2));
            }
            &:hover {
              color: rgba(var(--main-2));
              i {
                background: rgba(var(--main-2));
                color: rgba(var(--white));
              }
            }
          }
        }
      }
      .foot {
        padding: 50px 60px;
        text-align: center;
        font-size: 18px;
        color: rgba(var(--white), 0.5);
        line-height: 27px;
        width: 100%;
        letter-spacing: 0.3px;
        span {
          flex-grow: 1;
        }
      }
    }
  }
}
</style>
