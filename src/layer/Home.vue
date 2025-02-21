<template>
  <div class="container">
        <div class="title">文章</div>
        
        <div class="article">
            <h2>我好像為什麼事情很悲哀，我想起“生命”</h2>
            <div class="flex">
            <div>
              <div class="flex">
                <div class="fake-person"></div>
                <div class="meta-text">{{ name }} {{ dateTime }}</div>
              </div>
              
                <div class="content">有什麼人能用綠竹作弓矢，射入雲空，永不落下？我之想像，猶如長箭，向...</div>
            </div>
              <div class="images">
                  <div class="fake-img"></div>
              </div>
            </div>
            <div class="actions">
              <label v-for="label in labelList" :key="label" class="label">{{label}}</label> 231 | 收藏 34 | 評論 34 | 觀看 786</div>
        </div>
        
        <div class="article">
            <h2>讓讓彷彿是一種美德，若想在眼前的實際生活！</h2>
            <div class="flex">
                <div class="fake-person"></div>
                <div class="meta-text">{{ name }} {{ dateTime }}</div>
              </div>
            <div class="content">一群客人擠在客廳裡，誰也不肯先坐，誰也不肯首座...</div>
            <div class="images">
              <div class="dashboard-fake-img"></div>
              <div class="dashboard-fake-img"></div>
              <div class="dashboard-fake-img"></div>
            </div>
            <div class="actions">
              <label v-for="label in secondLabelList" :key="label" class="label">{{label}}</label>> 231 | 收藏 34 | 評論 34 | 觀看 786</div>
        </div>
    </div>
</template>
<script lang="ts" setup>
import { ref } from "vue";
import dayjs from 'dayjs';
const name = ref("張傑攻");
const dateTime = dayjs(new Date()).format('YYYY.MM.DD');
const labelList = ref(['故事', '甄選優質', '點讚']);
const secondLabelList = ref(['散文', '點讚']);

</script>


<style>
 body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 90%;
            max-width: 600px;
            margin: 20px auto;
            background: #fff;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .title {
            text-align: center;
            font-size: 20px;
            font-weight: bold;
            padding-bottom: 10px;
            border-bottom: 2px solid #ddd;
        }
        .article {
            padding: 15px 0;
            border-bottom: 1px solid #eee;
        }
        .article:last-child {
            border-bottom: none;
        }
        .article h2 {
            font-size: 16px;
            margin: 0 0 5px;
        }
        .meta-text {
            color: #888;
            font-size: 12px;
            margin-left:4px;
        }
        .content {
            font-size: 14px;
            color: #333;
            margin: 10px 0;
        }
        .images {
            display: flex;
            gap: 5px;
        }
        .images img {
            width: 30%;
            border-radius: 5px;
        }
        .actions {
            font-size: 12px;
            color: #888;
            margin-top: 5px;
        }

        .fake-person {
          width: 20px;
          height: 20px;
          border-radius: 100%;
          background-color:#888;
        }

        .fake-img {
          width: 140px;
          height: 100px;
          border-radius: 4px;
          background-color:#888;
        }
        .dashboard-fake-img {
          width: 33.33%;
          height: 160px;
          border-radius: 4px;
          background-color:#888;
        }
        .flex {
          display: flex;
          align-items: center;
        }
        .label {
          margin-left: 4px;
          margin-right: 4px;
          background-color:antiquewhite;
        }
</style>
