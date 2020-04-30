<template>
<body>
  <header>
    <div class="container">
      <div class="header-left">Progate</div>
      <div class="header-right">
        <a class="login" @click="isActive=!isActive">ログイン</a>
        <template class="dropdown" v-if="isActive">
          <div
            class="dropdown-tables"
            style="position: fixed;left:50%;transform: translate(-50%,20%);"
          >
            <h3>アカウントを作成</h3>
            <input placeholder="ユーザー名" />
            <input placeholder="メールアドレス" />
            <input placeholder="パスワード" />
            <input class="contact-submit" type="submit" />
            <div class="social-login">
              <div class="border-or">
                <div class="border">
                  <span class="or">または</span>
                </div>
              </div>
              <div class="btn-wrapper">
                <a href="#" class="btn facebook" style="width: 100%">
                  <span class="fab fa-facebook-f"></span>Facebookで登録
                </a>
                <a href="#" class="btn twitter" style="width: 100%">
                  <span class="fab fa-twitter"></span>Twitterで登録
                </a>
              </div>

              <!-- <div class="google"></div> -->
              <!-- <div class="facebook">
                <span class="fab fa-facebook-f"></span>
              </div>
              <div class="twitter">
                <span class="fab fa-twitter"></span>
              </div>-->
            </div>
          </div>
        </template>
        <div class="dropdown-overlay" @click="isActive = !isActive" v-if="isActive"></div>
      </div>
    </div>
  </header>
  <div class="top-wrapper">
    <div class="container">
      <h1>
        LEARN TO CODE.
        <br />LEARN TO BE CREATIVE.
      </h1>
      <p class="sub-intro">
        Progateはオンラインプログラミング学習サービスです。
        <br />初心者にもやさしいスライドとレッスンで、ウェブサービスを作りながら学んでいきましょう。
      </p>
      <a href="#" class="btn signup">新規登録はこちら</a>
      <p>or</p>
      <a href="#" class="btn facebook">
        <span class="fab fa-facebook-f"></span>Facebookで登録
      </a>
      <a href="#" class="btn twitter">
        <span class="fab fa-twitter"></span>Twitterで登録
      </a>
    </div>
  </div>

  <div class="lesson-wrapper">
    <div class="container">
      <div class="heading">
        <h2>Learn Where to Get Started!</h2>
      </div>

      <div class="lessons">
        <div class="lesson">
          <div class="lesson-icon">
            <div class="image-htmlCss"></div>
            <p>HTML & CSS</p>
          </div>
          <p class="text-contents">ウェブページの作成に使用される言語です。HTMLとCSSを組み合わせることで、静的なページを作り上げることができます。</p>
        </div>
        <div class="lesson">
          <div class="lesson-icon">
            <div class="image-jQuery"></div>
            <p>jQuery</p>
          </div>
          <p
            class="text-contents"
          >素敵な動きを手軽に実装できるJavaScriptライブラリです。 アニメーション効果をつけたり、Ajax（エイジャックス）を使って外部ファイルを読み込んだりと色々なことができます。</p>
        </div>
        <div class="lesson">
          <div class="lesson-icon">
            <div class="image-ruby"></div>
            <p>Ruby</p>
          </div>
          <p
            class="text-contents"
          >オープンソースの動的なプログラミング言語で、 シンプルさと高い生産性を備えています。大きなWebアプリケーションから小さな日用ツールまで、さまざまなソフトウェアを作ることができます。</p>
        </div>
        <div class="lesson">
          <div class="lesson-icon">
            <div class="image-php"></div>
            <p>PHP</p>
          </div>
          <p
            class="text-contents"
          >オープンソースの動的なプログラミング言語で、 シンプルさと高い生産性を備えています。大きなWebアプリケーションから小さな日用ツールまで、さまざまなソフトウェアを作ることができます。</p>
        </div>
      </div>
    </div>
  </div>

  <div class="message-wrapper">
    <div class="container">
      <div class="heading">
        <h2>さぁ、あなたもProgateでプログラミングを学んでみませんか?</h2>
        <h3>Let's learn to code, learn to be creative!</h3>
      </div>
      <span class="btn message">さっそく開発する</span>
    </div>
  </div>

  <footer>
    <div class="container">
      <div class="footer-left">Progate</div>
      <p>Learn to Code, Learn to be Creative.</p>
    </div>
  </footer>
</body>
</template>

<script>
export default {
  data: function() {
    return {
      isActive: false
    };
  }
};
</script>

<style lang="scss">
@include media(xl) {
  .top-wrapper {
    padding: 280px 0 280px 0;
    background-image: url("~assets/work-731198_1920.jpg");
    background-size: cover;
    color: white;
    text-align: center;
    h1 {
      opacity: 0.7;
      font-size: 45px;
      letter-spacing: 5px;
    }
    p {
      opacity: 0.7;
      margin-bottom: 15px;
    }
    .container {
      width: 100%;
      margin: 0 auto;
      .btn {
        padding: 8px 24px;
        color: white;
        display: inline-block;
        opacity: 0.8;
        border-radius: 4px;
      }
      .btn:hover {
        opacity: 1;
      }
      .fab {
        margin-right: 5px;
      }
      .signup {
        background-color: #239b76;
        margin-top: 15px;
        margin-bottom: 15px;
      }
      .facebook {
        background-color: #3b5998;
        margin-right: 10px;
      }
      .twitter {
        background-color: #55acee;
      }
    }
  }

  header {
    height: 65px;
    width: 100%;
    background-color: rgba(34, 49, 52, 0.9);
    position: fixed;
    top: 0;
    z-index: 10;
    .dropdown-overlay {
      z-index: 0;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 120%;
      background-color: rgba(0, 0, 0, 0.75);
    }
    .logo {
      width: 124px;
      margin-top: 20px;
    }
    .header-left {
      float: left;
      color: rgba(255, 255, 255, 0.9);
      font-size: 200%;
      padding: 10px 10px 20px 20px;
    }
    .header-right {
      float: right;
      background-color: rgba(255, 255, 255, 0.3);
      transition: all 0.5s;
    }
    .header-right:hover {
      background-color: rgba(255, 255, 255, 0.5);
    }
    .header-right a {
      line-height: 65px;
      padding: 0 25px;
      color: white;
      display: block;
    }
    .dropdown-tables {
      color: #000000;
      background-color: #ffffff;
      z-index: 8;
      font-size: 120%;
      text-align: center;
      border-radius: 8px;
      width: 40%;
      padding: 2% 0;
    }
    input {
      width: 70%;
      margin-top: 10px;
      margin-bottom: 10px;
      padding: 3%;
      font-size: 20px;
      border: 1px solid #dee7ec;
      border-radius: 4px;
      color: #889eab;
    }
    .contact-submit {
      background-color: #dee7ec;
      color: #889eab;
    }
    .social-login {
      .border-or {
        position: relative;
        .border {
          border-top: 1px solid rgba(168, 168, 168, 0.5);
          padding: 5px;
          width: 70%;
          margin-left: auto;
          margin-right: auto;
          margin-top: 4%;
          margin-bottom: 4%;
        }
        .or {
          position: absolute;
          bottom: 0.2%;
          left: 42%;
          right: 42%;
          @include media(m) {
            left: 25%;
            right: 25%;
          }
          background-color: #ffffff;
          padding: 0 5px;
          font-size: 80%;
        }
      }
      .btn-wrapper {
        width: 70%;
      margin-left: auto;
      margin-right: auto;
      font-size: 106%;
        .btn {
          line-height: 30%;
          padding: 4% 24px;
          margin-bottom: 2%;
          color: white;
          display: inline-block;
          opacity: 0.8;
          border-radius: 4px;
        }
        .btn:hover {
          opacity: 1;
        }
        .fab {
          margin-right: 5px;
        }
        // .signup {
        //   background-color: #239b76;
        //   margin-top: 15px;
        //   margin-bottom: 15px;
        // }
        .facebook {
          background-color: #3b5998;
          margin-right: 10px;
        }
        .twitter {
          background-color: #55acee;
        }
      }
    }
  }

  .lesson-wrapper {
    height: 580px;
    background-color: #f7f7f7;
    text-align: center;
    .heading {
      padding-top: 80px;
      padding-bottom: 50px;
      color: #5f5d60;
    }

    $box-size: 50%;

    .lesson {
      float: left;
      width: 25%;
      padding: 0 3%;
      .lesson-icon {
        position: relative;
        p {
          font-size: 200%;
          transform: translate(0, -10%);
        }
        .image-htmlCss {
          padding: $box-size;
          background-color: #ff4b4b;
        }
        .image-jQuery {
          padding: $box-size;
          background-color: #9f4bff;
        }
        .image-ruby {
          padding: $box-size;
          background-color: #14c8ff;
        }
        .image-php {
          padding: $box-size;
          background-color: #4bff69;
        }
      }
    }
    .lesson-icon p {
      position: absolute;
      top: 44%;
      width: 100%;
      color: white;
    }
    .text-contents {
      width: 80%;
      display: inline-block;
      margin-top: 15px;
      font-size: 13px;
      color: #4e4e4e;
    }
  }

  .heading h3 {
    font-weight: normal;
  }
  .message-wrapper {
    padding-bottom: 80px;
    text-align: center;
    .heading {
      padding-top: 80px;
      padding-bottom: 50px;
      color: #5f5d60;
    }
    .message {
      padding: 15px 40px;
      background-color: #5dca88;
      cursor: pointer;
      box-shadow: 0 7px #1a7940;
    }
    .message:active {
      position: relative;
      top: 7px;
      box-shadow: none;
    }
  }

  footer {
    padding: 30px 20px;
    border-top: 1px solid #eee;
    footer p {
      color: #b3aeb5;
      font-size: 12px;
    }
    .footer-left {
      color: rgba(124, 253, 124, 0.9);
      font-size: 200%;
    }
  }
}

@include media(s) {
  .top-wrapper {
    padding: 140px 0 140px 0;
    background-image: url("~assets/work-731198_1920.jpg");
    background-size: cover;
    color: white;
    text-align: center;
    h1 {
      opacity: 0.7;
      font-size: 45px;
      letter-spacing: 5px;
      padding-bottom: 80px;
    }
    .sub-intro {
      padding-bottom: 40px;
      font-weight: 500;
    }
    p {
      opacity: 0.7;
      margin-bottom: 15px;
    }
    .container {
      width: 90%;
      margin: 0 auto;
      .btn {
        width: 100%;
        color: white;
        display: inline-block;
        opacity: 0.8;
        border-radius: 4px;
        font-size: 110%;
      }
      .btn:hover {
        opacity: 1;
      }
      .fab {
        margin-right: 5px;
      }
      .signup {
        background-color: #239b76;
        margin-top: 15px;
        margin-bottom: 15px;
      }
      .facebook {
        background-color: #3b5998;
        margin-bottom: 15px;
      }
      .twitter {
        background-color: #55acee;
      }
    }
  }

  header {
    height: 65px;
    width: 100%;
    background-color: rgba(34, 49, 52, 0.9);
    position: fixed;
    top: 0;
    z-index: 10;
    .logo {
      width: 124px;
      margin-top: 20px;
    }
    .header-left {
      float: left;
      color: rgba(255, 255, 255, 0.9);
      font-size: 200%;
      padding: 10px 10px 20px 20px;
    }
    .header-right {
      float: right;
      background-color: rgba(255, 255, 255, 0.3);
      transition: all 0.5s;
    }
    .dropdown-tables {
      color: #000000;
      background-color: #ffffff;
      z-index: 8;
      font-size: 120%;
      text-align: center;
      border-radius: 8px;
      width: 90%;
      padding: 2% 0;
    }
    .header-right:hover {
      background-color: rgba(255, 255, 255, 0.5);
    }
    .header-right a {
      line-height: 65px;
      padding: 0 25px;
      color: white;
      display: block;
    }
    .btn-wrapper {
      width: 70%;
      margin-left: auto;
      margin-right: auto;
      font-size: 106%;
      .btn {
        padding: 4% 0;
        margin-bottom: 2%;
      }
    }
  }

  .lesson-wrapper {
    height: 2170px;
    background-color: #f7f7f7;
    text-align: center;
    .heading {
      padding-top: 80px;
      padding-bottom: 80px;
      color: #5f5d60;
    }
    .lessons {
      display: block;
      // all: initial;
    }

    $box-height: 30%;

    .lesson {
      display: block;
      width: 100%;
      padding: 0 5%;
      .lesson-icon {
        position: relative;
        p {
          font-size: 250%;
          transform: translate(0, -35%);
        }
        .image-htmlCss {
          padding: $box-height;
          background-color: #ff4b4b;
        }
        .image-jQuery {
          padding: $box-height;
          background-color: #9f4bff;
        }
        .image-ruby {
          padding: $box-height;
          background-color: #14c8ff;
        }
        .image-php {
          padding: $box-height;
          background-color: #4bff69;
        }
      }
    }
    .lesson-icon p {
      position: absolute;
      top: 44%;
      width: 100%;
      color: white;
    }
    .text-contents {
      width: 80%;
      margin-top: 10px;
      margin-bottom: 85px;
      font-size: 20px;
      color: #4e4e4e;
    }
  }

  .heading h3 {
    font-weight: normal;
  }
  .message-wrapper {
    padding-bottom: 80px;
    text-align: center;
    .heading {
      padding: 80px 20px 50px 20px;
      padding-bottom: 50px;

      color: #5f5d60;
    }
    .message {
      padding: 15px 40px;
      background-color: #5dca88;
      cursor: pointer;
      box-shadow: 0 7px #1a7940;
    }
    .message:active {
      position: relative;
      top: 7px;
      box-shadow: none;
    }
  }

  footer {
    padding: 30px 20px;
    border-top: 1px solid #eee;
    footer p {
      color: #b3aeb5;
      font-size: 12px;
    }
    .footer-left {
      color: rgba(124, 253, 124, 0.9);
      font-size: 200%;
    }
  }
}
</style>