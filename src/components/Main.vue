<template>
    <main>
        <section class="tabArea">
            <div class="tab">
                <ul class="tab-gnb">
                    <li><a @click="activetab=1" :class="[ activetab === 1 ? 'active' : '' ]">Tab1</a></li>
                    <li><a @click="activetab=2" :class="[ activetab === 2 ? 'active' : '' ]">Tab2</a></li>
                    <li><a @click="activetab=3" :class="[ activetab === 3 ? 'active' : '' ]" class="tab-btn-3">Tab3</a>
                    </li>
                </ul>
            </div>
            <div class="tab-content">
                <ul>
                    <li v-if="activetab === 1" class="content">
                        <div>Lorem ipsum dolor, sit amet consectetur adipisicing elit. <br>
                            Architecto modi ex molestiae obcaecati reprehenderit magni iusto unde sunt iste,<br>
                            quidem consequuntur doloribus molestias quia, similique rem rerum corrupti libero dicta?
                        </div>
                    </li>
                    <li v-if="activetab === 2" class="content">
                        <div style="color: blue">
                            <p>돈까스 사주세요.</p>
                        </div>
                    </li>
                    <li v-if="activetab === 3" class="content">
                        <div style="color: green">
                            <p>간짜장 사주세용</p>
                        </div>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>

<script>
    export default {
        name: 'Main',
        data() {
            return {
                activetab: 1,
            }
        },
    }
</script>

<style>
    .tabArea {
        max-width: 500px;
        margin: auto;
    }

    .tab {
        overflow: hidden;
        margin-bottom: -19px;
    }

    .tab-gnb {
        display: flex;
        padding: 30px 0;
    }

    .tab-gnb a {
        padding: 12px 24px;
        cursor: pointer;
        border: 1px solid #ccc;
        border-right: none;
        background-color: #f1f1f1;
        font-size: 16px;
        transition: background-color 0.2s;
    }

    .tab-gnb .tab-btn-3 {
        border-right: 1px solid #ccc;
    }

    .tab-gnb a:hover {
        background-color: #ccc;
        color: #000;
    }

    .tab-gnb a.active {
        background-color: #fff;
        color: #000;
        border-bottom: 1px solid #fff;
        font-weight: bold;

    }

    .tab-content {
        padding: 30px;
        text-align: left;
        border: 1px solid #ccc;
        box-shadow: 3px 3px 6px #e1e1e1;
    }

    .tab-content .content {
        font-size: 14px;
        color: #666;
    }
</style>