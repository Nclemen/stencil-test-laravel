<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        <form name="testform" action="http://example-app.test/receive" method="post">
                            <input type="hidden" name="_token" :value="csrf">
                            <input type="hidden" name="name" value="jack">

                            <svn-label owner>file input</svn-label>
                            <svn-file-input el_id="fileupload"></svn-file-input>

                            <svn-label>number input:</svn-label>
                            <svn-number-input></svn-number-input>

                            <svn-label>text input:</svn-label>
                            <svn-text-input></svn-text-input>

                            <svn-label>textarea:</svn-label>
                            <svn-textarea form="testform"></svn-textarea>

                            <svn-label>checkbox:</svn-label>
                            <svn-radio-input options='[{"name":"option 1", "value":"Option 1"}]'></svn-radio-input>
                            <input type="submit">
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        },
        data() {
            return {
                csrf: document.querySelector('meta[name="csrf-token"]').getAttribute('content')
            }
        }
    }
</script>
