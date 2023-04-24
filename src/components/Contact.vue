<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data(): { name: string, email: string, message: string, errorMessages: string[] } {
        return {
            name: "",
            email: "",
            message: "",
            errorMessages: []
        }
    },

    // To be implemented
    methods: {
        sendEmail(): void {
            if (this.validateInput()) {
                // Send email
                console.log("Sending email...")
                console.log(this.name)
                console.log(this.email)
                console.log(this.message)
            }
        },

        validateInput(): boolean {
            // Prototype validation subject to change
            const emailRegex = new RegExp("[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*@(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?");
            let isValid = true

            this.errorMessages = []

            if (!emailRegex.test(this.email)) {
                this.errorMessages.push("Your email address looks invalid. Please double check and try again.")
                isValid = false
            }
            if (this.name.length < 2) {
                this.errorMessages.push("Name must be at least 2 characters long")
                isValid = false
            }
            if (this.message.length < 10) {
                this.errorMessages.push("Message must be at least 10 characters long")
                isValid = false
            }

            return isValid
        }
    }
})
</script>

<template>
    <div id="contact" class="container">
        <h1 class="fw-bold text-center text-white">Contact me</h1>
        <p class="text-center text-white">If you have any questions or want to work with me, feel free to shoot me a quick message.</p>
        <div v-if="errorMessages.length > 0">
            <ul class="list-group">
                <li v-for="errorMessage in errorMessages" class="list-group-item list-group-item-danger mt-1">{{ errorMessage }}</li>
            </ul>
        </div>
        <form>
            <div class="row">
                <div class="col-md-6 mt-3">
                    <div class="form-floating">
                        <input v-model="email" type="email" class="form-control" id="email" placeholder="name@example.com">
                        <label for="email"><i class="bi bi-envelope-fill"></i> Email address</label>
                    </div>
                </div>
                <div class="col-md-6 mt-3">
                    <div class="form-floating">
                        <input v-model="name" type="text" class="form-control" id="name" placeholder="Your Name">
                        <label for="name"><i class="bi bi-person-fill"></i> Name</label>
                    </div>
                </div>
            </div>

            <div class="form-floating mt-3">
                <textarea v-model="message" class="form-control" placeholder="Leave a message here" id="message" style="height: 200px;"></textarea>
                <label for="message"><i class="bi bi-pencil-fill"></i> Message</label>
            </div>

            <div class="d-flex justify-content-end mt-3">
                <button @click="sendEmail" id="contact-button" class="btn btn-primary" type="button">Send <i class="bi bi-send"></i></button>
            </div>
        </form>
    </div>
</template>

<style scoped>
.list-group,
.list-group-item {
    border-radius: 10px;
    transition: all 0.2s ease-in-out;
}

.list-group-item:hover {
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
    transform: translateY(-3px);
}

.form-floating input,
.form-floating textarea {
    background-color: transparent;
    border: none;
    border-bottom: 2px solid #cccccc;
    border-radius: 0;
    padding: 8px 0;
    color: #ffffff;
    padding-left: 14px;
}

.form-floating label {
    color: #ffffff;
}

.btn-primary {
    border: none;
    border-radius: 10px;
}

.btn-primary:hover {
    background-color: rgb(16, 170, 62);
}
</style>

