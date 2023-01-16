<script lang="ts">
</script>

<div>
  <div class="boxed">
    <ion-icon name="alarm-outline" />
  </div>
</div>

<style>
  .boxed {
    width: 50px;
    height: 50px;
    display: flex;
    border-radius: 100px;
    font-size: 30px;
    align-items: center;
    justify-content: center;
    color: #e73c3c;
    position: relative;   
  }
  /* currentColor nó lấy theo giá trị thuộc tính color */
  .boxed:before {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    border-radius: inherit;
    background-color: currentColor;
    opacity: 0.1;
  }
</style>
