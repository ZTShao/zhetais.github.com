<template>
    <el-row>
        <el-col class="image" :xs="{span: 24}" :sm="{span: 14}">
            <img src="./assets/avatar.jpg" alt="avatar">
        </el-col>
        <el-col class="text" :xs="{span: 24}" :sm="{span: 10}">
            <div>
                <h1 class="title">{{title}}</h1>
                <p class="description">{{description}}</p>
                <p class="current">{{current}}</p>
                <p class="hobbies">{{hobbies}}</p>
                <hr>
                <p class="email">{{email}}</p>
                <p class="tel">{{tel}}</p>
                <p class="wechat">{{wechat}}</p>
                <p class="qq">{{qq}}</p>
                <hr>
                <div class="icons">
                    <a href="https://github.com/ZTShao">
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-github"></use>
                        </svg>
                    </a>

                    <a href="https://www.linkedin.com/in/zhetai-shao-779308172/">
                        <svg class="icon" aria-hidden="true">
                            <use xlink:href="#icon-linkedin"></use>
                        </svg>
                    </a>
                </div>
                <p class="footer">By <a style="color: aqua" href="https://github.com/ZTShao">Zhetai Shao </a><span
                        class="love">❤</span> 有一天会再发芽。</p>
            </div>
        </el-col>
    </el-row>
</template>

<script>
    import Config from './config'

    export default {
        name: 'app',
        data() {
            return {
                ...Config
            }
        }
    }
</script>

<style>
    @keyframes fadeIn {
        0% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }

    @keyframes slideInRight {
        0% {
            opacity: 0;
            transform: translateX(100px);
        }
        100% {
            opacity: 1;
            transform: translateX(0);
        }
    }

    * {
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }

    body {
        background: #303133;
    }

    .image {
        display: flex;
        justify-content: center;
        align-items: center;
        background: silver;
    }

    .image img {
        width: 100%;
        opacity: 1;
        animation: fadeIn 3s;
    }

    .text {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 0 20px;
        text-align: center;
        background: black;
        font-family: "Helvetica";
        color: white;
        animation: slideInRight 3s;
    }

    @media (min-width: 768px) {
        .text, .image {
            height: 100vh;
        }
    }

    .title {
        margin-bottom: 30px;
        font-size: 45px;

    }

    .description {
        font-size: 20px;
        color: #7F9191;
    }

    .current {
        font-size: 20px;
        color: #7F9191;
    }

    .hobbies {
        margin-top: 20px;
        color: #7F9191;
    }

    .email {
        margin-top: 20px;
    }

    .tel {
        margin-top: 8px;
    }

    .wechat {
        margin-top: 8px;
    }

    .qq {
        margin-top: 8px;
    }

    .footer {
        margin-top: 150px;
    }

    .icons a {
        margin: 0 8px;
        color: white;
        font-size: 2em;
    }

    hr {
        margin-top: 30px;
        margin-bottom: 30px;
    }

    .love {
        color: red;
    }
</style>
