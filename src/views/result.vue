<template>
    <common id="result">
        <div class="app-inner containner">
            <menu-tree class="center-menu"
                       :menuList="menuList"
                       menuTitle="教学成果"
                       @change="changeMenu"></menu-tree>
            <div class="app-inner-right">
                <div v-show="this.currentIndex === 0">
                    <img class="news-img"
                         src="../../static/images/news_img.png">
                    <div class="news-title">虚拟仿真实验教学队伍实验教学水平和成果</div>
                    <div class="news-common-time">发布时间:2019-04-08 17:49:20</div>
                    <div class="news-content">
                        <p>
                            兰州交通大学轨道交通信息与控制虚拟仿真实验教学中心以国家级教学团队为基础，以国家级有突出贡献的中青年专家、运用国家级人才培养模式创新实验区培养模式，由教学、科研、专业技术人员和系统维护支持人员组成，形成了一支结构合理、实践经验丰富、专兼结合、互通互融的高水平实验教学和管理队伍。拥有国家级教学团队1个，甘肃省高等学校教学名师4人，国家级精品课程3门，省级精品课程8门，国家级特色专业4个，省级特色专业3个。近年来，出版教材20余部，发表教改论文30余篇，获得省级教学成果13项，获得省、市、厅科技进步奖32项、发明专利26项，近3年指导的学生获得各类学科竞赛188项
                        </p>
                    </div>
                </div>
                <div v-show="this.currentIndex === 1">

                </div>
            </div>
        </div>
    </common>
</template>

<script>
export default {
    data() {
        return {
            menuList: [
                {
                    name: '教学科研成果',
                    list: [
                        {
                            name: '教学名师'
                        },
                        {
                            name: '教学成果奖'
                        },
                        {
                            name: '精品课程'
                        },
                        {
                            name: '特色专业'
                        },
                        {
                            name: '教学团队'
                        },
                        {
                            name: '专著教材'
                        }
                    ]
                },
                {
                    name: '学生学习效果',
                    list: []
                },
                {
                    name: '科研促进教学',
                    list: [
                        {
                            name: '科研获奖'
                        },
                        {
                            name: '发明专利'
                        }
                    ]
                }
            ],
            currentIndex: 0
        }
    },
    methods: {
        changeMenu(index) {
            this.currentIndex = index
        }
    }
}
</script>

<style lang="less">
@import url('../../static/css/base');
</style>
