<script setup>
import { onMounted } from 'vue';


const modal = defineProps({
    patientId: String,
    patientName: String,
    hospitalNumber: String
})

</script>

<template>
    <div class="modal fade modal-md" id="initiatePatientModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title text-primary">Initiate Patient Visit</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <div class="form-outline form-white mb-3 px-2">
                        <p aria-label="User" name="user">
                            You are about to intiate {{ modal.hospitalNumber + ' ' + modal.patientName }}'s visit with the doctor.
                        </p>
                    </div>
                    <div class="form-outline form-white mb-3 px-2">
                        <span>Do you want to continue?</span>
                    </div>
                </div>
                <div class="modal-footer px-5">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">
                        <i class="bi bi-x-circle me-1"></i>
                        No
                    </button>
                    <button type="button" class="btn bg-primary text-white initiate-patient-btn">
                        <i class="bi bi-check-circle me-1"></i>
                        Yes
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>