<template>
  <div class="partnership">
    <div class="topbar">
      <p>Наши партнеры</p>
      <span>Нас уже выбрали</span>
    </div>
    <div class="slider-hero">
      <div class="main">
        <div class="slider d-none slider-for">
          <div><h3>1</h3></div>
          <div><h3>2</h3></div>
          <div><h3>3</h3></div>
          <div><h3>4</h3></div>
          <div><h3>5</h3></div>
        </div>
        <div class="slider slider-nav">
          <div class="imgSpace">
            <div class="imageFit">
              <img src="../assets/img/logo.svg" alt="" />
            </div>
          </div>
          <div class="imgSpace">
            <div class="imageFit">
              <img src="../assets/img/logo_tassay.svg" alt="" />
            </div>
          </div>
          <div class="imgSpace">
            <div class="imageFit">
              <img src="../assets/img/kargo63.png" alt="" />
            </div>
          </div>
          <div class="imgSpace">
            <div class="imageFit">
              <img src="../assets/img/logo-pc.png" alt="" />
            </div>
          </div>
          <div class="imgSpace">
            <div class="imageFit">
              <img src="../assets/img/logo.png" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.partnership {
  padding-top: 7%;
  width: 100%;
  background: rgba(var(--pseudo-white));
  position: relative;
  z-index: 0;
  background-image: linear-gradient(
    to top,
    rgba(54, 32, 77, 0.03) 0%,
    rgba(54, 32, 77, 0.03) 33%,
    rgba(var(--pseudo-white), 1) 66%,
    rgba(var(--pseudo-white), 1) 100%
  );
  .topbar {
    padding: 0 7% 3.8%;
    width: 100%;
    text-align: center;
    p {
      font-size: clamp(28px, 3.5vw, 70px);
      line-height: normal;
    }
    span {
      font-size: 20px;
      line-height: 27px;
      letter-spacing: 0.3px;
      opacity: 0.7;
    }
  }
  .slider-hero {
    padding: 0 7% 7%;
    .main {
      font-family: Arial;
      width: 100%;
      display: block;
    }
    .slider-nav {
      .imgSpace {
        padding: 0.76%;
        background: #fff;
        border-right: 1px solid rgba(var(--black), 0.05);
        cursor: pointer;
        .imageFit {
          color: rgba(var(--black));
          width: 100%;
          height: 150px;

          position: relative;
          text-align: center;
          display: flex;
          img {
            width: 100%;
            height: 100%;
            object-fit: contain;
            padding: 5%;
          }
        }
      }
    }
  }
}
@media (max-width: 479px) {
  .partnership {
    padding-top: 0; //e
    padding-bottom: 30px; //e
    background: rgba(var(--white)); //e
    background-image: linear-gradient(
      to top,
      rgba(54, 32, 77, 0.03) 0%,
      rgba(54, 32, 77, 0.03) 0,
      rgba(var(--pseudo-white), 0) 0,
      rgba(var(--pseudo-white), 0) 0
    ); //e
    .topbar {
      padding: 30px 25px; //e
      text-align: start; //e
      span {
        font-size: 18px; //e
      }
    }
    .slider-hero {
      padding: 0; //e
      .slider-nav {
        .imgSpace {
          padding: 20px; //e
          .imageFit {
            height: 130px;
            img {
              padding: 10px;
            }
          }
        }
      }
    }
  }
}
@media (min-width: 480px) and (max-width: 767px) {
  .partnership {
    padding-top: 0; //e
    padding-bottom: 20px; //e
    background: rgba(var(--white)); //e
    background-image: linear-gradient(
      to top,
      rgba(54, 32, 77, 0.03) 0%,
      rgba(54, 32, 77, 0.03) 0,
      rgba(var(--pseudo-white), 0) 0,
      rgba(var(--pseudo-white), 0) 0
    ); //e
    .topbar {
      padding: 20px 25px; //e
      text-align: start; //e
      span {
        font-size: 18px; //e
      }
    }
    .slider-hero {
      padding: 0; //e
      .slider-nav {
        .imgSpace {
          padding: 20px; //e
          .imageFit {
            height: 140px;
            img {
              padding: 10px;
            }
          }
        }
      }
    }
  }
}
@media (min-width: 768px) and (max-width: 1023px) {
  .partnership {
    padding-top: 0; //e
    padding-bottom: 40px; //e
    background: rgba(var(--white)); //e
    background-image: linear-gradient(
      to top,
      rgba(54, 32, 77, 0.03) 0%,
      rgba(54, 32, 77, 0.03) 0,
      rgba(var(--pseudo-white), 0) 0,
      rgba(var(--pseudo-white), 0) 0
    ); //e
    .topbar {
      padding: 50px 30px; //e
      text-align: start; //e
      span {
        font-size: 19px; //e
      }
    }
    .slider-hero {
      padding: 0; //e
      .slider-nav {
        .imgSpace {
          padding: 20px; //e
          .imageFit {
            img {
              padding: 10px;
            }
          }
        }
      }
    }
  }
}
</style>

<script>
import $ from "jquery";

export default {
  setup() {
    $(document).ready(function () {
      console.log("scipt");
      let w = window.innerWidth;
      let n = 3;
      // window.onresize = function () {
      //   console.log(w + " resize");
      // };

      $(".slider-for").slick({
        slidesToShow: 1,
        slidesToScroll: 1,
        arrows: false,
        fade: true,
        asNavFor: ".slider-nav",
      });
      window.onload = function () {
        if (w < 480) {
          n = 1;
          console.log("srabotalo " + n);
        } else if (w >= 480 && 768 > w) {
          n = 2;
          console.log("srabotalo " + n);
        } else {
          n = 3;
          console.log("srabotalo " + n);
        }

        console.log(n + " check n");
        $(".slider-nav").slick({
          slidesToShow: n, //count
          slidesToScroll: 1,
          asNavFor: ".slider-for",
          dots: true,
          focusOnSelect: true,
        });
      };

      $("a[data-slide]").click(function (e) {
        e.preventDefault();
        var slideno = $(this).data("slide");
        $(".slider-nav").slick("slickGoTo", slideno - 1);
      });
      console.log("worked");
    });
  },
};
</script>
