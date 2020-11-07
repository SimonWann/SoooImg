<template>
    <div id="scale">
        <b-list-group-item id="scaleLink" href="#">
            <div id="b1">
                <button @click.prevent>+</button>
                <button disabled="disabled">{{scaleNum}}%</button>
                <button @click.prevent>-</button>
            </div>
            <div id="b2">
                <b-dropdown text="List " offset="">
                     <b-dropdown-item>打开</b-dropdown-item>
                      <b-dropdown-item>另存为</b-dropdown-item>
                       <b-dropdown-item>图片属性</b-dropdown-item>
                        <b-dropdown-item>首选项</b-dropdown-item>
                </b-dropdown>
                <div id="mtoolbar">
                    <span>-</span>
                    <span @click.prevent="close">x</span>
                </div>
            </div>
            
        </b-list-group-item>
        
    </div>
</template>
<script>

export default {
    data: function() {
        return {
            scaleNum: 100
        }
    },
    methods: {
        close() {
            
        }
    }
}
</script>
<style lang="less">
@gray: #343a40;
@lgray: lighten(@gray, 10%);
@dgray: darken(@gray, 10%);
.nodrag{
    -webkit-app-region: no-drag;
} 
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
    #scale{
        -webkit-app-region: drag;
        #scaleLink{
            margin: 0px;
            padding: 1.5vh 1.7vw;
            background: #343a40;
            display: flex;
            justify-content: space-between;
            height: 6.5vh;
            border-bottom-width: 2px;
            box-shadow: 0px 1px 3px @dgray;
        }
        #b1{
            button{
                .btnGtk;
                .nodrag;
                &:hover{
                    background: @lgray;

                }
                &:focus{
                    outline: 0px solid #000;
                }
                &:active{
                    background: @dgray;
                }
                &:first-of-type{
                    border-top-right-radius: 0px;
                    border-bottom-right-radius: 0px;
                }
                &:nth-of-type(2){
                    border-radius: 0px;
                    background: @dgray;
                }
                &:last-of-type{
                    border-top-left-radius: 0px;
                    border-bottom-left-radius: 0px;
                }
            }
        }
        #b2{
            display: flex;
            justify-content: space-between;
            div{
                height: 31px;
            }
            button{
                .nodrag;
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
            ul{
                background: @gray;
                border: 1px solid #000;
                box-shadow: 0px 0px 2px #141a20;
                padding: 10px 10px;
                position: absolute;
                left: -5vw;
                
            }
            a{
                font-size: 5px;
                background: @gray;
                color: #fff;
                padding: 10px 0px 10px 5px;
                border-radius: 3px;
                &:hover{
                    background: @lgray;
                }
            }
            #mtoolbar{
                .nodrag;
                margin: 0px 0px 0px 30px;
                color: #fff;
                align-self: center;
                display: flex;
                span{
                    font-size: 20px;
                    padding: 0px 7px;
                    margin-right: 10px;
                    &:last-child{
                        font-size: 15px;
                        align-self: center;
                    }
                    &:hover{
                        background: lighten(@gray, 30%);
                        border-radius: 27px;
                        box-shadow: 0px 0px 5px lighten(@gray, 30%);
                    }
                    &:active{
                         background: lighten(@gray, 10%);
                        border-radius: 27px;
                        box-shadow: 0px 0px 5px lighten(@gray, 10%);
                    }
                    
                }
                
            }
        }
        
    }
    
</style>