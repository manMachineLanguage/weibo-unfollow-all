# -
批量取消微博关注
微博点击头像到个人主页，再到我的关注，选择批量管理，复制以下内容到浏览器控制台回车执行
```
function deleteMessage() {
  // 下箭头
  let iDom = document.getElementsByClassName('woo-checkbox-shadow')[0];
  if (iDom) {
    iDom.click();
    setTimeout(() => {
    // 删除点击
      document.getElementsByClassName('woo-button-main woo-button-line woo-button-default woo-button-s woo-button-round FollowContent_stbtn_2WkHD')[0]?.click() ;
    }, 10) 
    setTimeout(() => {
      // 确认删除框 确认点击
      document.getElementsByClassName('woo-button-main woo-button-flat woo-button-primary woo-button-m woo-button-round woo-dialog-btn')[0]?.click();
      console.log(true)
      setTimeout(() => {
        // 重复执行
        deleteMessage()
      }, 100)
    }, 300)
  }
}
// 执行(想要提速可以多执行几次)
deleteMessage()
```

https://github.com/BraisedAlice404/weibo-delete-all-dynamics 直接在这上面改了改，感谢！
