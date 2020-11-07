<template>
    <div id="sidebar">
        <b-button id="sideBarbtn" v-b-toggle.sidebar-right>
            <b-icon icon="calendar2-event-fill"></b-icon>
        </b-button>
        <b-sidebar id="sidebar-right" title="" right shadow>
            <div class="px-3 py-2">
                <h3>
                    {{title}}
                </h3>
                <ul>
                    <li>大小： {{size}}</li>
                    <li>类型：     {{type}}</li>
                    <li>文件大小： {{storage}}</li>
                    <li>文件夹：   {{director}}</li>
                    <br/>
                    <li>光圈：     {{info.diaphragm}}</li>
                    <li>曝光： {{info.exposure}}</li>
                    <li>焦距： {{info.focalDistance}}</li>
                    <li>ISO： {{info.iso}}</li>
                    <li>测光： {{info.photometry}}</li>
                    <li>相机： {{info.camera}}</li>
                    <br/>
                    <li>日期： {{date}}</li>
                    
                </ul>
            </div>
        </b-sidebar>
    </div>
</template>
<script>
export default {
    data: function() {
        return {
            title: '属性',
            size: '',
            type: '',
            storage: '',
            director: '',
            info: {
                diaphragm: '',
                exposure: '',
                focalDistance: '',
                iso: '',
                photometry: '',
                camera: ''
            },
            date: ''
        }
    }
}
</script>
<style lang="less">
@gray: #343a40;
@lgray: lighten(@gray, 10%);
@dgray: darken(@gray, 10%);
.btnGtk{
    font-size: 12px;
    border-radius: 5px;
    background: #343a40;
    color: #fff;
    border: 1px solid #000;
    box-shadow: 0px 0px 2px #141a20;
    padding: 5px 13px;
    height: 30px;
}
    #sidebar{
        
        #sideBarbtn{
            position: absolute;
            left: 1.5vw;
            top: 8vh;
            .btnGtk;
            &:hover{
                    background: @lgray;

                }
                &:focus{
                    outline: 0px solid #000;
                }
                &:active{
                    background: @dgray;
                }
        }
        #sidebar-right{
            position: reletive;
            top: 6.7vh;
            height: 93.2vh;
            h3{
                padding: 2vh 3vw;
            }
            ul{
                padding: 5vh 3vw;
            }
            li{
                list-style: none;
            }
        }
    }
</style>