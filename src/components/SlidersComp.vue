<template>
  <div class="w-full relative main">
    <div v-if="isModalOpen" ref="modal-bg" class="modal-bg">
      <div class="modal-1" ref="modal1">
        <button class="close-x" @click="closeModal">x</button>
        <div class="content">
          <form action="">
            <p class="mb-2.5">Расчет стоимости</p>
            <span
              >Заполните форму, наш менеджер свяжется с Вами в ближайшее
              время.</span
            >
            <input
              class="modal-price mt-5"
              type="text"
              placeholder="Ваше имя"
            />
            <input
              type="number"
              class="modal-price numbers"
              placeholder="Телефон"
            />
            <label for="sm-1" class="mb-4"><span>Вид услуги:</span></label>
            <br />
            <select name="services " id="sm-1">
              <option value="auto">Автомобильные перевозки</option>
              <option value="air">Авиа перевозки</option>
              <option value="train">Железнодорожные перевозки</option>
            </select>
            <div class="m-details">
              <input
                type="text"
                class="modal-price"
                placeholder="Общий вес, кг"
              />
              <input
                type="text"
                class="modal-price"
                placeholder="Общий объем, м3"
              />
              <input type="text" class="modal-price" placeholder="Откуда" />
              <input type="text" class="modal-price" placeholder="Куда" />
            </div>
            <textarea
              name=""
              class="numbers modal-price"
              id=""
              cols="30"
              rows="10"
              placeholder="Подробное описание"
            ></textarea>
            <div class="flex items-center mb-4">
              <input class="checkbox mr-2" type="checkbox" />
              <span
                >Ознакомлен(на) с
                <a class="user-agree" href=""
                  >пользовательским соглашением</a
                ></span
              >
            </div>
            <button class="btnPrice mb-0 mt-0">
              Отправить
              <i class="fa-solid fa-caret-right iconPrice"></i>
            </button>
          </form>
        </div>
      </div>
    </div>

    <div class="content">
      <div
        id="carouselExampleIndicators"
        class="carousel slide w-full"
        data-bs-ride="carousel"
      >
        <div class="carousel-indicators">
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="0"
            class="active"
            aria-current="true"
            aria-label="Slide 1"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="1"
            aria-label="Slide 2"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="2"
            aria-label="Slide 3"
          ></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img
              src="../assets/img/truck.jpg"
              class="d-block w-100"
              alt="..."
            />
            <div class="absolute slide-text h-15 text-white text-center">
              <div class="flex-col justify-end">
                <p>Доставим в самые кратчайшие сроки</p>
                <p>Автомобильные перевозки</p>
                <button @click="isModalOpen = true" class="btnPrice">
                  Расчет Стоимости
                  <i class="fa-solid fa-caret-right iconPrice"></i>
                </button>
                <p>
                  Транспортно-логистическая компания организует грузоперевозки
                  по всему миру
                </p>
              </div>
            </div>
          </div>
          <div class="carousel-item">
            <img
              src="../assets/img/plane.jpg"
              class="d-block w-100"
              alt="..."
            />
            <div class="absolute slide-text h-15 text-white text-center">
              <div class="flex-col justify-end">
                <p>Доставим в самые кратчайшие сроки</p>
                <p>Авиа перевозки</p>

                <button @click="isModalOpen = true" class="btnPrice">
                  Расчет Стоимости
                  <i class="fa-solid fa-caret-right iconPrice"></i>
                </button>
                <p>
                  Транспортно-логистическая компания организует грузоперевозки
                  по всему миру
                </p>
              </div>
            </div>
          </div>
          <div class="carousel-item">
            <img
              src="../assets/img/train.jpg"
              class="d-block w-100"
              alt="..."
            />
            <div class="absolute slide-text h-15 text-white text-center">
              <div class="flex-col justify-end">
                <p>Доставим в самые кратчайшие сроки</p>
                <p>Железнодорожные перевозки</p>

                <button @click="isModalOpen = true" class="btnPrice">
                  Расчет Стоимости
                  <i class="fa-solid fa-caret-right iconPrice"></i>
                </button>
                <p>
                  Транспортно-логистическая компания организует грузоперевозки
                  по всему миру
                </p>
              </div>
            </div>
          </div>
        </div>
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide="prev"
        >
          <i class="fas fa-chevron-left text-black text-xs"></i>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide="next"
        >
          <i class="fas fa-chevron-right text-black text-xs"></i>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.main {
  .btnPrice {
    margin-bottom: 70px;
    margin-top: 25px;
  }
  .modal-bg {
    position: fixed;
    z-index: 10;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    overflow-y: auto;

    background: rgba(var(--black), 0.5);

    display: flex;
    .modal-1 {
      position: relative;
      z-index: 1;
      background: rgba(255, 255, 255, 1);
      padding: 40px 50px;
      border-radius: 2px;
      width: 650px;
      margin: auto;
      .close-x {
        position: absolute;
        right: 10px;
        top: 10px;
        height: 40px;
        width: 40px;
        font-size: 22px;
      }
      .content {
        width: 100%;
        form {
          display: block;
          width: 100%;
          p {
            font-size: 31px;
            line-height: normal;
          }
          span {
            font-size: 18px;
            color: rgba(var(--black), 0.7);
          }
          input,
          select {
            width: 100%;
          }
          .checkbox {
            width: fit-content;
          }
          textarea {
            width: 100%;
            height: 150px;
          }
          .modal-price,
          select {
            padding: 8px 20px;
            border: 1px solid rgba(var(--black), 0.1);
            border-radius: 2px;
            min-height: 60px;
            font-size: 17px;
            margin-bottom: 15px;
          }
          .user-agree {
            color: #7badff !important;
            text-decoration: underline;
            &:hover {
              text-decoration: none;
            }
          }
          .m-details {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;

            input {
              width: 48.5%;
            }
          }
        }
      }
    }
  }
  .content {
    position: relative;
    z-index: 0;
    .carousel-indicators {
      background: rgba(0, 0, 0, 0.5);
      width: fit-content;
      margin: 0;
      left: 50%;
      transform: translateX(-50%);
      bottom: 10px;
      border-radius: 10px;
      padding: 2px;
      button {
        width: 4px !important;
        height: 4px !important;
        border-radius: 100%;
        margin-left: 2px !important;
        margin-right: 2px !important;
        border-top: none !important;
        border-bottom: none !important;
      }
    }

    .carousel-indicators button.active {
      width: 10px !important;
      border-radius: 3px;
      box-shadow: 1px 1px 2px rgb(0 0 0 / 90%);
    }

    .carousel-control-prev,
    .carousel-control-next {
      height: fit-content;
      width: fit-content;
      color: #000;
      top: 50%;
      transform: translateY(-50%);
      background: #fff;
      padding: 10.5px 14px;
      border-radius: 100%;
      opacity: 0.7;
      border: 1px solid rgb(114, 111, 111);
    }

    .carousel:hover .carousel-control-next,
    .carousel:hover .carousel-control-prev {
      opacity: 1;
    }

    .carousel-control-prev {
      left: 1rem;
    }

    .carousel-control-next {
      right: 1rem;
    }

    .carousel-inner {
      height: 100%;

      img {
        height: 780px;
        object-fit: cover;
      }

      .slide-text {
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);
        position: relative;
        z-index: 1;
        width: 80%;
        flex-direction: column;
        flex-grow: 1;

        p:nth-child(1) {
          font-size: 22px;
          opacity: 0.8;
        }
        p:nth-child(2) {
          font-size: clamp(28px, 4.1vw, 85px);
          letter-spacing: 0.7px;
          line-height: normal;
        }
        // button {

        // }
        p:nth-child(4) {
          padding-bottom: 50px;
          font-size: 18px;
          opacity: 0.6;
          font-weight: 400;
        }
      }
    }
    .carousel-item:after {
      content: "";
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0%;
      left: 0%;
      background: rgba(var(--main-2), 0.3);
      z-index: 0;
    }
  }
}
@media (max-width: 479px) {
  .main {
    .modal-bg {
      .modal-1 {
        padding: 30px 25px; //edited
        margin: auto 20px; //edited
        .content {
          form {
            p {
              font-size: 25px; //edited
              padding-right: 30px;
            }
            span {
              font-size: 17px; //edi
            }
            textarea {
              height: 120px; //edited
            }
            .modal-price,
            select {
              padding: 8px 15px; //edited
              min-height: 55px; //ed
            }
            .m-details {
              input {
                width: 100%; //ed
              }
            }
          }
        }
      }
    }
    .content {
      .carousel-inner {
        img {
          height: 451px;
        }
        .slide-text {
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);

          p:nth-child(1) {
            font-size: 19px;
          }
          p:nth-child(4) {
            display: none;
          }
        }
      }
      .carousel-control-prev {
        left: 50%;
        transform: translate(-100%, -200%);
      }

      .carousel-control-next {
        right: 50%;
        transform: translate(100%, -200%);
      }
      .carousel-control-prev,
      .carousel-control-next {
        height: fit-content;
        width: fit-content;
        color: #fff;
        bottom: 20px;
        top: 100%;
        background: rgb(255, 255, 255);
        padding: 10.5px 14px;
        border-radius: 0;
        opacity: 0.8;
        border: 1px solid rgba(114, 111, 111, 0);
      }
    }
  }
}
@media (min-width: 480px) and (max-width: 767px) {
  .main {
    .modal-bg {
      position: fixed;
      z-index: 10;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      overflow-y: auto;

      background: rgba(var(--black), 0.5);

      display: flex;
      .modal-1 {
        position: relative;
        z-index: 1;
        background: rgba(255, 255, 255, 1);
        padding: 40px; //edited
        border-radius: 2px;
        width: 100%;
        display: flex;
        margin: 34px 30px; //edited
        .close-x {
          position: absolute;
          right: 10px;
          top: 10px;
          height: 40px;
          width: 40px;
          font-size: 22px;
        }
        .content {
          width: 100%;
          form {
            display: block;
            width: 100%;
            p {
              font-size: 25px; //edited
              line-height: normal;
            }
            span {
              font-size: 18px;
              color: rgba(var(--black), 0.7);
            }
            input,
            select {
              width: 100%;
            }
            .checkbox {
              width: fit-content;
            }
            textarea {
              width: 100%;
              height: 150px;
            }
            .modal-price,
            select {
              padding: 8px 20px;
              border: 1px solid rgba(var(--black), 0.1);
              border-radius: 2px;
              min-height: 60px;
              font-size: 17px;
              margin-bottom: 15px;
            }
            .user-agree {
              color: #7badff !important;
              text-decoration: underline;
              &:hover {
                text-decoration: none;
              }
            }
            .m-details {
              display: flex;
              flex-wrap: wrap;
              justify-content: space-between;

              input {
                width: 48.5%;
              }
            }
          }
        }
      }
    }
    .content {
      .carousel-inner {
        img {
          height: 380px;
        }
        .slide-text {
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);

          p:nth-child(1) {
            font-size: 19px;
          }
          p:nth-child(4) {
            display: none;
          }
        }
      }
    }
  }
}
@media (min-width: 768px) and (max-width: 1023px) {
  .main {
    .modal-bg {
      position: fixed;
      z-index: 10;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      overflow-y: auto;

      background: rgba(var(--black), 0.5);

      display: flex;
      .modal-1 {
        position: relative;
        z-index: 1;
        background: rgba(255, 255, 255, 1);
        padding: 50px; //asd
        border-radius: 2px;
        width: 100%;
        display: flex;
        margin: 95px 50px; //asd
        .close-x {
          position: absolute;
          right: 10px;
          top: 10px;
          height: 40px;
          width: 40px;
          font-size: 22px;
        }
        .content {
          width: 100%;
          form {
            display: block;
            width: 100%;
            p {
              font-size: 31px;
              line-height: normal;
            }
            span {
              font-size: 18px;
              color: rgba(var(--black), 0.7);
            }
            input,
            select {
              width: 100%;
            }
            .checkbox {
              width: fit-content;
            }
            textarea {
              width: 100%;
              height: 150px;
            }
            .modal-price,
            select {
              padding: 8px 20px;
              border: 1px solid rgba(var(--black), 0.1);
              border-radius: 2px;
              min-height: 60px;
              font-size: 17px;
              margin-bottom: 15px;
            }
            .user-agree {
              color: #7badff !important;
              text-decoration: underline;
              &:hover {
                text-decoration: none;
              }
            }
            .m-details {
              display: flex;
              flex-wrap: wrap;
              justify-content: space-between;

              input {
                width: 48.5%;
              }
            }
          }
        }
      }
    }
    .content {
      .carousel-inner {
        img {
          height: 451px;
        }
        .slide-text {
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);

          p:nth-child(1) {
            font-size: 19px;
          }
          p:nth-child(4) {
            display: none;
          }
        }
      }
    }
  }
}
</style>

<script>
import "bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";

// import { ref } from "vue";
// import { onClickOutside } from "@vueuse/core";
// import Modal1 from "./Modal1Comp.vue";
// const isModalOpen = ref(false);
// const modal1 = ref(null);

// onClickOutside(modal1, () => (isModalOpen.value = false));

export default {
  // components: { Modal1 },

  data() {
    return {
      isModalOpen: false,

      // modal1,
    };
  },
  methods: {
    closeModal() {
      this.isModalOpen = false;
    },
  },
  mounted() {
    let vm = this;
    document.addEventListener("click", function (item) {
      if (item.target === vm.$refs["modal-bg"]) {
        vm.closeModal();
      }
    });
  },
};
</script>
