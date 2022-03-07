# Day7  導覽列

### Learned

- margin-auto 會自動分配 margin
- navbar item hover 動畫
  - 透過 left right 的變化就可以做到動態底線
  - 透過 transform 做到 hover 時選項移動，要注意 inline 屬性無法作用，因此改變物件屬性為 flex
  ```scss
    .main-nav {
      display: flex;
      margin: auto;
      a {
        font-size: 1.25rem;
        margin: 0px 10px;
        position: relative;
        transition: 0.3s;

        &:after {
          content: "";
          position: absolute;
          left: 50%;
          right: 50%;
          bottom: -5px;
          height: 0;
          border-bottom: 1px solid white;
          transform: translateY(0px);
          transition: 0.3s;
        }
        &:hover {
          transform: translateY(-5px);
          &:after {
            left: 0;
            right: 0;
          }
        }
      }
    }
  ```

- DEMO
<img src="../demo/demo-goldfish-layout-day7.gif" width="1440px"/>