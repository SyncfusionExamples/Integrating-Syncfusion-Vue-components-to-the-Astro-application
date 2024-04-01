<template>
    <div>
        <div class="control-section">
            <div class="control-wrapper">
                <div class="default-section">
                    <div class="forum">
                        <div class="questionSection">
                            <div class="raiser">
                                <table>
                                    <tbody>
                                        <tr>
                                            <td>
                                                <div class="questionar blog-avatar"> </div>
                                            </td>
                                            <td>
                                                <div class="Questionarname"> Kimberly </div>
                                            </td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                            <div class="questionHeader">
                                <div class="header">
                                    How to add a custom item to the toolbar of RichTextEditor
                                </div>
                                <div class="detailsQuestion">Posted on May 7, 2018 6.10 PM</div>
                                <div class="explain">
                                    I want to add a custom icon, “code-mirror” to the toolbar of RichTextEditor and
                                    display the RichTextEditor content in code-mirror format.
                                </div>
                                <div class="tags">
                                    <div class="tagSection">
                                        <table>
                                            <tbody>
                                                <tr>
                                                    <td>
                                                        <div class="tag"> HTML </div>
                                                    </td>
                                                    <td>
                                                        <div class="tag"> JavaScript </div>
                                                    </td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </div>
                                    <div class="questionLikes">
                                        <table>
                                            <tbody>
                                                <tr>
                                                    <td>
                                                        <span class="e-icon e-like questionSide">
                                                            <img class="e-icon"
                                                                src="https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/like.svg"
                                                                alt="like">
                                                            <span>Like</span>
                                                        </span>
                                                    </td>
                                                    <td>
                                                        <span class="e-icon e-dislike">
                                                            <img class="e-icon"
                                                                src="https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/dislike.svg"
                                                                alt="dislike">
                                                            <span>Dislike</span>
                                                        </span>
                                                    </td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </div>
                                </div>
                            </div>
                            <div class="separator"></div>
                        </div>
                        <div class="answerSection">
                            <div class="answerCount">1 Answer</div>
                            <div class="answer">
                                <table>
                                    <tbody>
                                        <tr>
                                            <td rowspan="2">
                                                <div class="logos blog-avatar"> </div>
                                            </td>
                                            <td>
                                                <div class="authorname">Mabel Weber</div>
                                            </td>
                                        </tr>
                                        <tr>
                                            <td>
                                                <div class="detailsAnswer">Answered on May 7, 2018 6.30 PM</div>
                                            </td>
                                        </tr>
                                    </tbody>
                                </table>
                                <div class="posting">
                                    To add a custom icon
                                    <b>code-mirror</b> to the Toolbar, you have to use template option of the
                                    <b>toolbarSettings</b>. To know more about adding custom icons, refer to
                                    <a href='https://ej2.syncfusion.com/home/' target='_blank'>custom tool</a> sample of
                                    RTE.
                                </div>
                                <div class="likeAnswer">
                                    <table>
                                        <tbody>
                                            <tr>
                                                <td>
                                                    <span class="e-icon e-like">
                                                        <img class="e-icon"
                                                            src="https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/like.svg">
                                                        <span>Like</span>
                                                    </span>
                                                </td>
                                                <td>
                                                    <span class="e-icon e-dislike">
                                                        <img class="e-icon"
                                                            src="https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/dislike.svg">
                                                        <span>Dislike</span>
                                                    </span>
                                                </td>
                                            </tr>
                                        </tbody>
                                    </table>
                                </div>
                                <div class="separator"></div>
                            </div>
                        </div>

                        <div id="createpostholder">
                            <form novalidate="novalidate">
                                <ejs-richtexteditor ref="rteInstance" v-model="value" v-bind:value="value"
                                    placeholder="Write a reply"></ejs-richtexteditor>
                                <div id="buttonSection">
                                    <table>
                                        <tbody>
                                            <tr>
                                                <td>
                                                    <ejs-button v-on:click="clickSubmit" :isPrimary="isPrimary"
                                                        id="rteSubmit" type="button" value="Reply">Reply</ejs-button>
                                                </td>
                                                <td>
                                                    <ejs-button v-on:click="clickCancel" id="rteCancel" value="Cancel"
                                                        type="button">Cancel</ejs-button>
                                                </td>

                                            </tr>
                                        </tbody>
                                    </table>
                                </div>

                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>


    </div>
</template>
<style>
@import "@syncfusion/ej2-base/styles/material3.css";
@import "@syncfusion/ej2-inputs/styles/material3.css";
@import "@syncfusion/ej2-lists/styles/material3.css";
@import "@syncfusion/ej2-popups/styles/material3.css";
@import "@syncfusion/ej2-buttons/styles/material3.css";
@import "@syncfusion/ej2-navigations/styles/material3.css";
@import "@syncfusion/ej2-splitbuttons/styles/material3.css";
@import "@syncfusion/ej2-vue-richtexteditor/styles/material3.css";

.control-section {
    display: flex;
    height: 100vh;
}

.control-wrapper {
    margin: auto;
}

.tagSection {
    float: left;
}

.likeAnswer span.e-icon {
    float: left;
}

img.e-icon {
    width: 13px;
    height: 25px;
}

span.questionSide {
    margin-left: 24px;
    float: left;
}

.e-dislike {
    margin-left: 16px;
    float: left;
}

.questionHeader {
    margin-top: 12px;
    margin-bottom: 5px;
}

.header {
    font-size: 16px;
    font-family: roboto-Semibold, SegoeUI-Semibold;
    color: #000000;
    font-weight: bold;
    clear: both;
}

@media (max-width: 550px) {
    .forum {
        padding: 20px 20px 60px 20px;
    }
}

@media (min-width: 550px) {
    .forum {
        margin: 0 auto;
        width: 80%;
        border: 1px solid #d8d8c0;
        padding: 10px 90px 60px 90px;
        box-shadow: 2px 2px 2px 2px #f5f5ef;
    }

    .highcontrast .forum {
        border: 1px solid #fff;
    }
}

.e-like span {
    font-family: Helvetica, Times New Roman;
    color: #E3175A;
    font-size: 12px;
}

.e-dislike span {
    font-family: Helvetica, Times New Roman;
    color: #717171;
    font-size: 12px;
}

.detailsQuestion {
    font-size: 12px;
    font-family: roboto, SegoeUI;
    color: #575757;
    margin-top: 8px;
}

.explain {
    margin-top: 16px;
    font-size: 13px;
    font-family: roboto, SegoeUI;
    color: #000000;
}

.separator {
    margin-top: 5px;
    border-bottom: 1px solid #DADADA;
    margin-bottom: 5px;
}

.tags td:first-child div {
    margin-left: 0px;
}

.tag {
    color: #000000;
    padding: 3px 14px;
    background-color: #DDDDDD;
    font-size: 13px;
    margin-left: 8px;
    border-radius: 6px;
    float: left;
    text-transform: lowercase;
    font-family: roboto, SegoeUI;
}

.answerCount {
    color: #575757;
    margin-top: 24px;
    margin-bottom: 24px;
    font-family: roboto-Semibold, SegoeUI-Semibold;
    width: 63px;
}

.likeAnswer {
    margin-top: 13px;
}

.tags {
    margin-top: 10px;
    margin-bottom: 24px;
}

.questionar {
    background: url(https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/emp1.png);
}

.raiser {
    height: 34px;
}

.Questionarname {
    margin-top: 13px;
    float: left;
    font-weight: 500;
    margin-left: 10px;
}

.your-answer {
    color: #3b3b3b;
    font-weight: 300;
}

.rating {
    padding-left: 10px;
    margin-top: -95px;
}

.logos {
    background: url(https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/emp2.png);
}

.logo {
    background: url(https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/author.png) no-repeat scroll 0 0 transparent;
}

.emp1 {
    background: url(https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/1.png) no-repeat scroll 0 0 transparent;
}

.emp2 {
    background: url(https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/2.png) no-repeat scroll 0 0 transparent;
}

.emp3 {
    background: url(https://ej2.syncfusion.com/vue/demos/src/rich-text-editor/images/3.png) no-repeat scroll 0 0 transparent;
}

.blog-avatar {
    height: 32px;
    -ms-flex-line-pack: center;
    align-content: center;
    -ms-flex-align: center;
    align-items: center;
    background-color: #bcbcbc;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    border-radius: 50%;
    color: #fff;
    width: 32px;
}

.author {
    margin-bottom: 5px;
    height: 50px;
    margin-top: 5px;
}

.name {
    margin: 5px;
    float: left;
    color: blue;
}

.posting {
    clear: both;
    color: #000;
    line-height: 24px;
    margin-top: 12px;
    font-family: roboto, SegoeUI;
    font-size: 13px;
    overflow-wrap: break-word;
}

.authorname {
    font-family: SegoeUI-Semibold;
    color: #000;
    font-size: 13px;
}

.detailsAnswer {
    color: #575757;
    font-size: 12px;
    font-family: roboto, SegoeUI;
    margin-top: 7px;
}

button {
    margin-left: 10px;
}

#buttonSection {
    float: right;
    margin-top: 11px;
}

#buttonSection input {
    margin-right: 11px;
}

.authorname,
.detailsAnswer {
    margin-left: 11px;
}

.answerCount {
    color: #76766f;
    margin-top: 20px;
    margin-bottom: 12px;
}

.questDesc {
    min-height: 120px;
    width: 100%;
}

.answerHeader {
    border-bottom: 1px solid #ced1d1;
    margin-bottom: 20px;
    margin-top: -40px;
}

.answer {
    margin-top: 15px;
}

.editorholder h4 {
    padding: 15px 0;
}

#createpostholder {
    margin-top: 25px;
}
</style>
<script>
import { isNullOrUndefined as isNOU } from "@syncfusion/ej2-base";
import { RichTextEditorComponent, Link, Image, QuickToolbar, HtmlEditor, Toolbar, PasteCleanup, Table, Video, Audio } from "@syncfusion/ej2-vue-richtexteditor";
import { ButtonComponent } from '@syncfusion/ej2-vue-buttons';

export default {
    components: {
        'ejs-richtexteditor': RichTextEditorComponent,
        'ejs-button': ButtonComponent
    },
    data: function () {
        return {
            isPrimary: true,
            value: ''
        };
    },
    methods: {
        clickCancel: function () {
            var answerElement = this.$refs.rteInstance.$el.parentNode.querySelector('.e-content');
            answerElement.innerHTML = '';
            this.value = '';
            setTimeout(() => { this.$refs.rteInstance.ej2Instances.refresh(); });
        },
        clickSubmit: function () {
            var empCount = 0
            var answerElement = this.$refs.rteInstance.$el.parentNode.querySelector('.e-content');
            var comment = answerElement.innerHTML;
            var empList = ['emp1', 'emp2', 'emp3'];
            var nameList = ['Anne Dodsworth', 'Janet Leverling', 'Laura Callahan'];
            if (comment !== null && comment.trim() !== '' && (answerElement.innerText.trim() !== '' ||
                !isNOU(answerElement.querySelector('img')) || !isNOU(answerElement.querySelector('table')))) {
                var answer = document.querySelector('.answer');
                var cloneAnswer = answer.cloneNode(true);
                var authorName = cloneAnswer.querySelector('.authorname');
                var logo = cloneAnswer.querySelector('.logos');
                logo.classList.remove('logos');
                if (empCount < 3) {
                    logo.classList.add(empList[empCount]);
                    logo.classList.add('blog-avatar');
                    authorName.innerHTML = nameList[empCount];
                    empCount++;
                } else {
                    logo.classList.add('logo');
                    logo.classList.add('blog-avatar');
                    authorName.innerHTML = 'User';
                }
                var timeZone = cloneAnswer.querySelector('.detailsAnswer');
                var day = this.getMonthName(new Date().getMonth()) + ' ' + new Date().getDate();
                var hr = new Date().getHours() + ':' + new Date().getMinutes();
                if (new Date().getHours() > 12) {
                    hr = hr + ' PM';
                } else {
                    hr = hr + ' AM';
                }
                timeZone.innerHTML = 'Answered on ' + day + ', ' + new Date().getFullYear() + ' ' + hr;
                var postContent = cloneAnswer.querySelector('.posting');
                postContent.innerHTML = comment;
                var postElement = document.querySelector('.answerSection');
                postElement.appendChild(cloneAnswer);
                var countEle = document.querySelector('.answerCount');
                var count = parseInt(countEle.innerHTML, null);
                count = count + 1;
                countEle.innerHTML = count.toString() + ' Answers';
                answerElement.innerHTML = '';
                this.value = '';
                setTimeout(() => { this.$refs.rteInstance.ej2Instances.refresh(); });
            }
        },
        getMonthName: function (index) {
            var month = [];
            month[0] = 'January';
            month[1] = 'February';
            month[2] = 'March';
            month[3] = 'April';
            month[4] = 'May';
            month[5] = 'June';
            month[6] = 'July';
            month[7] = 'August';
            month[8] = 'September';
            month[9] = 'October';
            month[10] = 'November';
            month[11] = 'December';
            return month[index];
        }
    },
    provide: {
        richtexteditor: [Link, Image, QuickToolbar, HtmlEditor, Toolbar, PasteCleanup, Table, Video, Audio]
    }
}
</script>