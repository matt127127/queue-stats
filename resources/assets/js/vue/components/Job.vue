<template>
    <div>
        <table class="table table-responsive table-hover table-bordered">
            <thead>
            <tr>
                <th class="text-center">Attempt number</th>
                <th class="text-center">Status</th>
                <th class="text-center">Handling duration</th>
                <th class="text-center">Waiting duration</th>
                <th class="text-center">Queries duration</th>
                <th class="text-center">Queries count</th>
                <th class="text-center">Exception class</th>
                <th class="text-center">Exception message</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="attempt in rowData.attempts">
                <td class="text-center" v-text="attempt.attempt_number"></td>
                <td class="text-center" v-text="attempt.status"></td>
                <td class="text-center" v-text="attempt.handling_duration"></td>
                <td class="text-center" v-text="attempt.waiting_duration"></td>
                <td class="text-center" v-text="attempt.queries_duration"></td>
                <td class="text-center" v-text="attempt.queries_count"></td>
                <td class="text-center" v-text="attempt.exception_class"></td>
                <td class="text-center" v-text="attempt.exception_message"></td>
            </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
    export default {
        props: {
            rowData: {
                type: Object,
                required: true
            },
            rowIndex: {
                type: Number
            }
        }
    }
</script>