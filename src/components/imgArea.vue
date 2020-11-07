<template>
    <div id="icontainer">
      <b-img id="mainImg" src="https://picsum.photos/1024/400/?image=41" fluid alt="Responsive image"></b-img>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="less">
@border: 1px solid #343a40;
@borderImg: 10px solid #fff;
#icontainer{
  height: 93.5vh;
  width: 100vw;
  padding: 50px;
  background: #343a40;
  overflow: auto;
  &::-webkit-scrollbar{
    width: 10px;
    height: 10px;
    background: #fff;
  }
  &::-webkit-scrollbar-corner{
    
  }
  &::-webkit-scrollbar-thumb{
    width: 8px;
    height: 8px;
    background: #6c757d;
    border-radius: 2px;
  }
  &::-webkit-scrollbar-button{
    display: none;
  }
  &::-webkit-scrollbar-track{
    background: #e9ecef;
    border: 1px solid #c1c1c1;
    box-shadow: inset 0px 0px 4px #c1c1c1;
    border-radius: 2px;
  }
  #mainImg{
    border: @borderImg;
  }

}
</style>