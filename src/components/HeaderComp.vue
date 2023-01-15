<template>
  <div class="Header flex justify-between items-center">
    <div class="HeadLeft flex items-center">
      <i class="fa-solid fa-image mr-5"></i>
      <div>
        <p>BekLogistics</p>
        <span class="text-lg">Транспортно-логистическая компания</span>
      </div>
    </div>
    <div class="HeadRight flex items-center">
      <span class="font-bold numbers">+7 771 232 3307</span>
      <div
        class="relative ddbutton"
        @click="myFilter()"
        v-bind:class="{ active: isActive }"
      >
        <button>
          <i class="fa-solid fa-sort-down text-sm"></i>
        </button>
        <div class="modal-header">
          <!-- <div class="ddHeader-1 block">
            <span>Астана, Ленинский проспект, дом</span> <br />
            <a href="">Показать на карте</a>
          </div> -->
          <div class="ddHeader-2 flex items-center">
            <span class="numbers">+7 771 232 3307</span>
            <i class="fa-brands fa-telegram"></i>
            <i class="fa-brands fa-whatsapp"></i>
          </div>
          <div class="ddHeader-3">
            <span>test@example.com</span>
          </div>
          <div class="ddHeader-4">
            <span class="numbers">Работаем 24/7</span>
          </div>
          <div class="ddHeader-5">
            <img src="../assets/img/vk.svg" alt="" />
            <img src="../assets/img/insta.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.Header {
  position: relative;
  z-index: 1;
  background: #fff;
  padding: 25px 120px 25px 30px;
  .HeadLeft {
    i {
      font-size: 70px;
    }
    p {
      font-size: 33px;
    }
    span {
      font-size: 18px;
      color: #121212;
    }
  }
  .HeadRight {
    span {
      font-size: 23px;
      color: #121212;
    }
    .ddbutton {
      z-index: 2;
      &.active .modal-header {
        height: 300px;
        padding: 30px 55px 20px 55px;
      }
      &.active button i {
        transform: rotate(180deg) translateY(-25%);
      }
      button {
        padding: 15px 20.625px;
        border: 1px solid #121212;
        opacity: 0.4;
        border-radius: 3px;
        margin-left: 20px;
        i {
          transition: 0.4s all;
          display: flex;
        }
        &:hover {
          opacity: 1;
        }
      }
      .modal-header {
        width: 360px; //460
        background: #fff;
        top: 100%;
        right: 0;
        z-index: 1;
        position: absolute;
        padding: 0 55px;
        margin-top: 10px;
        transition: 0.4s all;
        display: block;
        height: 0;
        overflow: hidden;

        font-size: 18px;
        color: #121212;
        .ddHeader-2 {
          margin: 0 0 20px;
          span {
            font-size: 23px;
            font-weight: 700;
          }
          .fa-telegram {
            color: #229ed9;
            font-size: 40px;
            margin: 0 10px 0 20px;
          }
          .fa-whatsapp {
            color: #25d366;
            font-size: 40px;
          }
        }
        .ddHeader-3 {
          span {
            font-size: 18px;
          }
        }
        .ddHeader-4 {
          margin: 20px 0;
          span {
            font-size: 18px;
          }
        }
        .ddHeader-5 {
          display: flex;

          img {
            width: 40px;
            height: 40px;
            margin-left: 8px;
          }
          img:nth-child(1) {
            margin-left: 0;
          }
        }
      }
    }
  }
}

@media (max-width: 479px) {
  p {
    color: #d34825;
  }
  .Header {
    padding: 20px;
    flex-wrap: wrap;
    .HeadLeft {
      width: 100%;
      flex-wrap: wrap;
      padding-right: 45px;
      i {
        font-size: 60px;
      }
      p {
        font-size: 28px;
      }
    }
    .HeadRight {
      width: 100%;
      justify-content: flex-end;
      flex-direction: row-reverse;
      align-items: center;
      margin-top: 20px;
      span {
        font-size: 21px;
        color: #121212;
      }
      .ddbutton {
        &.active .modal-header {
          padding: 25px 25px 1px;
          height: 250px;
        }
        button {
          padding: 10px 15.625px;
          border-radius: 50%;
          margin-right: 20px;
          margin-left: 0;
        }
        .modal-header {
          padding: 0 25px;
          left: 0;
          width: 280px;
          .ddHeader-2 {
            span {
              font-size: 20px;
            }
          }
          .ddHeader-3 {
            span {
              font-size: 17px;
            }
          }
          .ddHeader-4 {
            margin: 15px 0;
            span {
              font-size: 17px;
            }
          }
        }
      }
    }
  }
}

@media (min-width: 480px) and (max-width: 767px) {
  p {
    color: #2536d3;
  }
  .Header {
    padding: 20px 25px;
    flex-wrap: wrap;
    .HeadLeft {
      width: 100%;
      padding-right: 50px;
      i {
        font-size: 65px;
      }
      p {
        font-size: 28px;
      }
    }
    .HeadRight {
      width: 100%;
      justify-content: flex-end;
      flex-direction: row-reverse;
      align-items: center;
      margin-top: 20px;
      span {
        font-size: 21px;
        color: #121212;
      }
      .ddbutton {
        &.active .modal-header {
          padding: 35px 35px 5px;
          height: 250px;
        }
        button {
          padding: 10px 15.625px;
          border-radius: 50%;
          margin-right: 20px;
          margin-left: 0;
        }
        .modal-header {
          padding: 0 35px;
          left: 0;

          .ddHeader-2 {
            span {
              font-size: 21px;
            }
          }
          .ddHeader-3 {
            span {
              font-size: 17px;
            }
          }
          .ddHeader-4 {
            margin: 15px 0;
            span {
              font-size: 17px;
            }
          }
        }
      }
    }
  }
}

@media (min-width: 768px) and (max-width: 1023px) {
  p {
    color: #25d366;
  }
  .Header {
    padding: 25px 90px 25px 25px;
    .HeadLeft {
      width: 100%;
      i {
        font-size: 65px;
      }
      p {
        font-size: 28px;
      }
    }
    .HeadRight {
      width: 100%;
      justify-content: flex-end;
      span {
        font-size: 21px;
        color: #121212;
      }
      .ddbutton {
        &.active .modal-header {
          padding: 40px 40px 5px;
        }
        button {
          padding: 10px 15.625px;
          border-radius: 50%;
        }
        .modal-header {
          padding: 0 40px;
          margin-top: 35px;
          z-index: 2;
          .ddHeader-2 {
            span {
              font-size: 21px;
            }
          }
          .ddHeader-3 {
            span {
              font-size: 17px;
            }
          }
          .ddHeader-4 {
            margin: 15px 0;
            span {
              font-size: 17px;
            }
          }
        }
      }
    }
  }
}
</style>
<script>
export default {
  name: "HeadersComp",

  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    myFilter: function () {
      this.isActive = !this.isActive;
      // some code to filter users
    },
  },
};
</script>
