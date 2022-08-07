<template>
  <div>
    欢迎来到我的主页~
    <li v-for="article in articList" :key="article.id">
      <router-link :to="{ path: '/ArticleInfo', query: { id: article.id } }">{{
        article.title
      }}</router-link>
    </li>
  </div>
</template>

<script>
export default {
  name: "MyvueView",
  data: function () {
    return {
      articList: [
        {
          id: "1",
          title: "新疆出现万马奔腾场景--我是master的新增",
          content:
            "7月16日，“天马之乡”新疆昭苏县，成群的骏马像离弦之箭，飞驰在一望无际的昭苏草原上，场面十分壮观！戳视频，一睹“万马奔腾”盛景。",
        },
        {
          id: "2",
          title: "奥运健儿时隔一年再战世界赛场",
          content:
            "去年7月，他们一同出征奥运；时隔一年，再次亮相世界赛场。世界田径锦标赛、WTT欧洲夏季系列赛相继开赛，不同赛场，继续为国争光，为他们喝彩！",
        },
      ],
    };
  },
};
</script>
