<script setup>
import { ref, reactive } from 'vue'
import { invoice1, invoice2 } from './data/data'
const data = reactive({
    sender: '',
    billTo: '',
    shipTo: '',
    invoiceNumber: '',
    date: '',
    dueDate: '',
    additionalNote: '',
    items: [
        { "description": "", "quantity": 0, "rate": 0, "amount": 0 }
    ],
    notes: '',
    terms: '',
    subtotal: '',
    tax: '',
    total: '',
    balanceDue: ''
})
</script>

<template>
    <section class="mx-auto container bg-white border border-gray-400 min-h-screen p-12">
        <div class="flex justify-between">
            <div class="flex flex-col space-y-5 w-1/2s">
                <div class=" ">
                    <img class="w-40"
                        src="https://www.shutterstock.com/image-vector/invoice-typographic-stamp-sign-badge-600w-1027820257.jpg"
                        alt="">
                </div>
                <p class="mt-5">
                    Sender
                </p>
                <textarea name="" id="" cols="30" rows="2"></textarea>
                <div class="flex space-x-2">
                    <div class="flex flex-col">
                        <span>Bill to</span>
                        <textarea name="" id="" cols="30" rows="2"></textarea>
                    </div>
                    <div class="flex flex-col">
                        <span>Ship to</span>
                        <textarea name="" id="" cols="30" rows="2"></textarea>
                    </div>
                </div>
            </div>
            <div class="flex flex-col w-1/2 items-end">
                <h1 class="mt-12 text-4xl uppercase text-right mb-5">Invoice</h1>
                <input class="w-[200px] text-right" type="text" placeholder="Invoice Number">
                <div class="mt-10 flex-y-5 text-right space-y-3 w-full">
                    <p>
                        <span>Date</span>
                        <input class="ml-2 w-[200px] ">
                    </p>
                    <p>
                        <span>Due Date</span>
                        <input class="ml-2 w-[200px]">
                    </p>
                    <p>
                        <span>Additional Note</span>
                        <input class="ml-2 w-[200px]" type="text">
                    </p>
                </div>
            </div>
        </div>
        <div class="mt-20">
            <table class="table-auto w-full">
                <tr class="bg-gray-800 text-left text-white">
                    <th class="p-2 pl-5 w-1/2">Item</th>
                    <th class="p-2">Quantity</th>
                    <th class="p-2">Rate</th>
                    <th class="p-2 w-[200px] text-right pr-5">Amount</th>
                </tr>
                <tr>
                    <td class="py-1">
                        <input class="w-full pl-5" type="text" placeholder="Description" />
                    </td>
                    <td class="">
                        <input class="w-full" type="number" placeholder="Quantity" />
                    </td>
                    <td class="">
                        <input class="w-full" type="number" placeholder="Rate">
                    </td>
                    <td class="py-1 pr-5 text-right text-gray-800">
                        $ 0.00
                    </td>
                </tr>
            </table>
            <button class="mt-5 bg-green-600 hover:bg-green-700 text-white font-bold py-2 px-4 rounded">
                Add More
            </button>
        </div>
        <div class="mt-[200px]">
            <div class="flex justify-between">
                <div class="flex flex-col space-y-5 w-1/2">
                    <span>Notes</span>
                    <textarea name="" id="" cols="30" rows="2"></textarea>
                    <span>Terms</span>
                    <textarea name="" id="" cols="30" rows="2"></textarea>
                </div>
                <div class="flex flex-col w-1/2 items-end">
                    <div class="mt-10 flex-y-5 text-right space-y-3 w-full">
                        <p>
                            <span>Subtotal</span>
                            <input readonly class="focus:ring-0 focus:ring-offset-0 text-right ml-2 pr-4 w-[200px] border-0"
                                placeholder="Subtotal">
                        </p>
                        <p>
                            <span>Tax</span>
                            <input type="number" class="tax text-right w-[200px] ml-2">
                        </p>
                        <p>
                            <span>Total</span>
                            <input readonly class="focus:ring-0 focus:ring-offset-0 text-right ml-2 pr-4 w-[200px] border-0"
                                placeholder="Total">
                        </p>
                        <p>
                            <span>Balace Due</span>
                            <input readonly class="focus:ring-0 focus:ring-offset-0 text-right ml-2 pr-4 w-[200px] border-0"
                                placeholder="Balance">
                        </p>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>

<style scoped>
input,
textarea {
    border: 1px solid #ddd !important;
    padding: 5px;
}</style>