<div class="flex items-center flex-col px-8">
    <h1 class="font-InterTight text-3xl font-semibold text-orange-950">Contact</h1>
    <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 items-stretch justify-center text-center gap-5 py-10">
        {#each contacts as {name, designation, organization, role, email, phone}}
            <div class="bg-white px-5 py-5 rounded-xl items-center justify-center flex flex-col shadow-2xl">
                <h1 class="text-orange-700 font-InterTight text-xl lg:text-2xl font-bold">{name}</h1>
                <h1 class="text-black lg:text-lg font-InterTight">{designation}</h1>
                <h1 class="text-black lg:text-lg font-semibold font-InterTight">{organization}</h1>
                <h1 class="text-orange-800 lg:text-xl font-InterTight font-semibold text-lg py-2">{role}</h1>
                <a href={`mailto:${email}`}><h1 class="text-blue-600 font-InterTight lg:text-lg">{email}</h1></a>
                {#if phone}
                <a href={`tel:${phone}`}><h1 class="text-stone-700 underline file:font-InterTight lg:text-lg">{phone}</h1></a>
                    
                {/if}

            </div>
        {/each}
    </div>
</div>

<script>
    import contacts from "./contactData";
</script>