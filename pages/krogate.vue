<template>
<body>
  <div class="header">
    <div class="header-logo">Krogate</div>
    <div class="header-list">
      <ul>
        <li>プログラミングとは</li>
        <li>学べるレッスン</li>
        <li>お問い合わせ</li>
      </ul>
    </div>
    <a class="menu-btn" @click="isActive=!isActive">︙</a>
    <template class="dropdown-table" v-if="isActive">
      <div style="position:fixed; left:50%; transform: translate(-50%,150%);z-index: 10">
        <ul class="dropdown-tables">
          <li>プログラミングとは</li>
          <li>学べるレッスン</li>
          <li>お問い合わせ</li>
        </ul>
      </div>
      <div class="dropdown-overlay" @click="isActive = !isActive" v-if="isActive"></div>
    </template>
  </div>

  <div class="main">
    <div class="copy-container">
      <h1>
        HELLO WORLD<span>.</span>
      </h1>
      <h2>
        プログラミングの世界へ
        <br />ようこそ
      </h2>
    </div>

    <div class="contents" v-if="!isActive">
      <h3 class="section-title">学べるレッスン</h3>

      <div class="lessons"></div>
      <div class="lesson">
        <div class="lesson-icon">
          <div class="image-htmlCss"></div>
          <p>HTML & CSS</p>
        </div>
        <!-- <p class="text-contents">HTML & CSS</p> -->
      </div>
      <div class="lesson">
        <div class="lesson-icon">
          <div class="image-jQuery"></div>
          <p>jQuery</p>
        </div>
        <!-- <p class="text-contents">jQuery</p> -->
      </div>
      <div class="lesson">
        <div class="lesson-icon">
          <div class="image-ruby"></div>
          <p>Ruby</p>
        </div>
        <!-- <p class="text-contents">Ruby</p> -->
      </div>
      <div class="lesson">
        <div class="lesson-icon">
          <div class="image-php"></div>
          <p>PHP</p>
        </div>
        <!-- <p class="text-contents">PHP</p> -->
      </div>
    </div>

    <!-- <div class="contents-item">
        <div class="image_htmlCss"></div>
        <p>HTML & CSS</p>
      </div>
      <div class="contents-item">
        <div class="image_php"></div>
        <p>PHP</p>
      </div>
      <br>
      <div class="contents-item">
        <div class="image_ruby"></div>
        <p>Ruby</p>
      </div>
      <div class="contents-item">
        <div class="image_swift"></div>
        <p>Swift</p>
    </div>-->
    <!-- </div> -->

    <div class="contact-form">
      <h3 class="section-title">お問い合わせ</h3>
      <p>メールアドレス（必須）</p>
      <input />
      <p>お問い合わせ内容（必須）</p>
      <textarea></textarea>
      <p>※必須項目は必ずご入力ください</p>
      <input class="contact-submit" type="submit" value="送信" />
    </div>
  </div>

  <div class="footer">
    <div class="footer-logo">Krogate</div>
    <div class="footer-list"  v-if="!isActive">
      <ul>
        <li>会社概要</li>
        <li>採用</li>
        <li>お問い合わせ</li>
      </ul>
    </div>
  </div>
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
@mixin box-size3 {
  padding: 110px;
  margin-right: 10px;
  @content;
}

@include media(xl) {
  .header {
    background-color: #26d0c9;
    color: #fff;
    height: 90px;
    width: 100%;
    .header-logo {
      float: left;
      font-size: 36px;
      padding: 20px 40px;
    }
    .header-list {
      float: right;
      li {
        float: left;
        padding: 33px 20px;
      }
    }
    .menu-btn {
      display: none;
    }
    .dropdown-tables {
      display: none;
    }
  }

  .main {
    padding: 100px 4%;
    .copy-container {
      h1 {
        font-size: 140px;
        span {
          color: #ff4a4a;
        }
      }

      h2 {
        font-size: 60px;
      }
    }
      .contents {
        width: 100%;
        height: 500px;
        margin-top: 100px;
        overflow-x: auto;
        .section-title {
          border-bottom: 2px solid #dee7ec;
          font-size: 28px;
          padding-bottom: 15px;
          margin-bottom: 50px;
        }

      $box-size: 120px;

      .lesson {
        float: left;
        width: 25%;
        padding: 0 4%;
        .lesson-icon {
          position: relative;
          .image-htmlCss {
            transform: rotateZ(45deg);
            padding: $box-size;
            background-color: #ff4b4b;
          }
          .image-jQuery {
            transform: rotateZ(45deg);
            padding: $box-size;
            background-color: #9f4bff;
          }
          .image-ruby {
            transform: rotateZ(45deg);
            padding: $box-size;
            background-color: #14c8ff;
          }
          .image-php {
            transform: rotateZ(45deg);
            padding: $box-size;
            background-color: #4bff69;
          }
        }
      }
      .lesson-icon p {
        position: absolute;
        top: 43%;
        width: 100%;
        color: white;
        font-size: 150%;
      }
      .text-contents {
        width: 80%;
        display: inline-block;
        margin-top: 45px;
        font-size: 23px;
        color: #4e4e4e;
      }
    }
    
    .contact-form {
      padding-top: 100px;
      .section-title {
        border-bottom: 2px solid #dee7ec;
        font-size: 28px;
        padding-bottom: 15px;
        margin-bottom: 50px;
      }
    }
    input,
    textarea {
      width: 400px;
      margin-top: 10px;
      margin-bottom: 30px;
      padding: 20px;
      font-size: 18px;
      border: 1px solid #dee7ec;
    }

    .contact-submit {
      background-color: #dee7ec;
      color: #889eab;
    }
  }
  .footer {
    background-color: #2f5167;
    color: #fff;
    height: 120px;
    padding: 40px;
    .footer-logo {
      float: left;
      font-size: 32px;
    }
    .footer-list {
      float: right;
      li {
        margin-bottom: 0%;
        transform: translate(0, -50%);
      }
    }
  }
}

@mixin box-size2 {
  padding: 130px;
  @content;
}

@include media(s) {
  .header {
    background-color: #26d0c9;
    color: #fff;
    height: 70px;
    .header-logo {
      float: left;
      font-size: 30px;
      padding: 4% 7% 4% 7%;
      font-weight: 500;
    }
    .header-list {
      display: none;
      float: right;
      li {
        float: left;
        padding: 33px 20px;
      }
    }
    .menu-btn {
      display: block;
      float: right;
      padding: 5%;
      transform: translate(0, -10%);
      font-weight: bold;
      font-size: 200%;
    }
    .dropdown-tables {
      display: block;
      z-index: 999;
      background-color: #26d0c9;
      padding: 20px;
      width: 160%;
      border-radius: 10px;
      text-align: center;
      margin-right: 0;
      transform: translate(-18.5%, -40%);
      li {
        color: #000000;
        background-color: #ffffff;
        z-index: 8;
        padding: 15px;
        font-size: 120%;
        font-weight: bold;
      }
      li:hover {
        background-color: #daffe1;
      }
    }
    .dropdown-overlay {
      z-index: 0;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 120%;
      background-color: rgba(0, 0, 0, 0.75);
    }
  }

  .main {
    all: initial;
    text-align: center;
    .copy-container {
      h1 {
        text-align: left;
        font-size: 435%;
        padding: 10% 2% 10% 6%;
        span {
          color: #ff4a4a;
        }
      }

      h2 {
        font-size: 170%;
        font-weight: normal;
      }
    }
    .contents {
      margin-top: 120px;
      overflow-x: visible;
      .section-title {
        border-bottom: 2px solid #dee7ec;
        font-size: 28px;
        padding-bottom: 15px;
        margin-bottom: 100px;
      }
      $box-size: 52%;

      .lesson {
        // display: block;
        width: 52%;
        padding: 5% 0%;
        transform: scale(1.2);
        margin-left: 22%;
        .lesson-icon {
          position: relative;
          .image-htmlCss {
            transform: rotateZ(45deg);
            padding: $box-size;
          }
          .image-jQuery {
            transform: rotateZ(45deg);
            padding: $box-size;
            background-color: #9f4bff;
          }
          .image-ruby {
            transform: rotateZ(45deg);
            padding: $box-size;
            background-color: #14c8ff;
          }
          .image-php {
            transform: rotateZ(45deg);
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
        font-size: 100%;
      }
      .text-contents {
        width: 80%;
        display: inline-block;
        margin-top: 45px;
        font-size: 23px;
        color: #4e4e4e;
      }
    }

    .contact-form {
      padding-top: 550px;
      .section-title {
        border-bottom: 2px solid #dee7ec;
        font-size: 28px;
        padding-top: 90px;
        padding-bottom: 15px;
        margin-bottom: 50px;
      }
    }
    input,
    textarea {
      width: 250px;
      margin-top: 10px;
      margin-bottom: 30px;
      padding: 20px;
      font-size: 10px;
      border: 1px solid #dee7ec;
    }

    .contact-submit {
      background-color: #dee7ec;
      color: #889eab;
    }
  }

  .footer {
    background-color: #2f5167;
    color: #fff;
    height: 120px;
    padding: 40px;
    .footer-logo {
      float: left;
      font-size: 32px;
    }
    .footer-list {
      float: right;
      li {
        margin-bottom: 0%;
        transform: translate(0, -50%, 0);
        // color:black;
      }
    }
  }
}
</style>