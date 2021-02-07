<template>
  <div class="post">
    <!-- header -->
    <header class="header section">
      <div class="header-author">
        <Avatar :size="40" :src="profile_img"></Avatar>
        <div class="author">
          <CustomText tag="b">{{ title }}</CustomText>
          <CustomText size="xsmall">İstanbul, Turkey</CustomText>
        </div>
      </div>
      <div class="header-more">
        <button type="button">
          <IconMore />
        </button>
      </div>
    </header>
    <!-- media -->
    <div class="post-media">
      <img :src="source" alt="" />
    </div>
    <!-- actions -->
    <div class="action-buttons section">
      <button type="button">
        <IconLike />
      </button>
      <button type="button">
        <IconComment />
      </button>
      <button type="button">
        <IconDirect />
      </button>
      <button type="button" class="action-save">
        <IconSave />
      </button>
    </div>
    <!-- like counter -->
    <div class="like-count section">
      <custom-text tag="b">1.328 beğenme</custom-text>
    </div>
    <!-- comment list -->
    <div class="comment-list section">
      <div class="single-comment">
        <custom-text tag="b">eneseren</custom-text>
        <custom-text class="comment">
          Vay be hiko baba.
        </custom-text>
      </div>
      <div class="single-comment">
        <custom-text class="all-comments">38 yorumun tümünü gör</custom-text>
      </div>
      <div class="single-comment">
        <custom-text tag="b">sedaaydin</custom-text>
        <custom-text class="comment">
          Kralsın.
        </custom-text>
      </div>
    </div>
    <!-- datetime -->
    <div class="datetime section">
      <custom-text tag="p" size="xsmall" class="time">
        6 Saat Önce
      </custom-text>
    </div>
    <hr />
    <!-- commentform -->
    <div class="comment-form section">
      <IconSmiley />
      <textarea
        aria-label="Yorum ekle..."
        placeholder="Yorum ekle..."
        class="comment-input"
        autocomplete="off"
        autocorrect="off"
      ></textarea>
      <button type="button">Paylaş</button>
    </div>
  </div>
</template>

<script>
import Avatar from "@/components/Avatar";
import CustomText from "@/components/CustomText";
import IconMore from "@/icons/more.svg";
import IconLike from "@/icons/like.svg";
import IconComment from "@/icons/comment.svg";
import IconDirect from "@/icons/direct-post.svg";
import IconSave from "@/icons/save.svg";
import IconSmiley from "@/icons/smiley.svg";
export default {
  name: "Post",
  components: {
    Avatar,
    CustomText,
    IconMore,
    IconLike,
    IconComment,
    IconDirect,
    IconSave,
    IconSmiley,
  },
  props: {
    source: {
      type: String,
      default:
        "https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-15/e35/144758061_1283165772051371_5558420204430163817_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_cat=1&_nc_ohc=h07NXygR-50AX9AeTIS&tp=1&oh=e2225de5282aa0f9a61ea0e178eaefcd&oe=603EB8FC",
    },
    title: {
      type: String,
      default: "Onur AKÇAY",
    },
    profile_img: {
      type: String,
      default:
        "https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-15/e35/144758061_1283165772051371_5558420204430163817_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_cat=1&_nc_ohc=h07NXygR-50AX9AeTIS&tp=1&oh=e2225de5282aa0f9a61ea0e178eaefcd&oe=603EB8FC",
    },
  },
};
</script>

<style scoped>
.comment-input {
  height: 18px;
  max-height: 80px;
  background: 0 0;
  border: 0;
  outline: 0;
  padding: 0;
  resize: none;
  width: 100%;
  margin-left: 16px;
  color: rgb(var(--i1d));
}
.comment-form {
  border-top: 1px solid rgba(var(--ce3, 239, 239, 239), 1);
  margin-top: 16px;
  min-height: 56px;
  display: flex;
  align-items: center;
}
.comment-form button {
  border: 0;
  color: rgba(var(--d69));
  font-weight: 700;
  display: inline;
  padding: 0;
  position: relative;
}
.all-comments {
  color: rgb(var(--f52));
}
.single-comment {
  margin: 2px 0px;
}
.datetime .time {
  text-transform: uppercase;
  color: rgb(var(--f52));
}
.comment-list {
  margin: 4px 0px;
  display: flex;
  flex-direction: column;
}
.comment-list .comment {
  margin-left: 0px;
}
.post {
  border-radius: 3px;
  border: 1px solid rgb(var(--b6a));
  margin-bottom: 60px;
}
.section {
  padding: 0px 16px;
}
.header {
  display: flex;
  align-items: center;
  height: 60px;
}
.header .header-author {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.header .header-author .author {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
}
.header .header-more {
  margin-left: auto;
}
.action-buttons {
  display: flex;
  align-items: center;
  height: 45px;
}
.action-buttons button {
  margin-right: 16px;
}
.action-save {
  margin-left: auto;
  margin-right: 0px!important;
}
</style>
