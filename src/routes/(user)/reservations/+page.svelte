<script>
    // Reservations Component

    import Reservations from "$lib/reservations.svelte";

    export let data;

    console.log(data);

    // $reservations = data.data["reservations"];

    // let dividedReservations = divideReservations($reservations);

    // $pastReservations = dividedReservations.pastReservations;

    // $upcomingReservations = dividedReservations.upcomingReservations;

    // function divideReservations(reservations) {
    //     let now = new Date();

    //     let pastReservations = [];

    //     let upcomingReservations = [];

    //     for (let i = 0; i < reservations.length; i++) {
    //         let reservation_time = new Date(reservations[i].reservation_time);

    //         if (reservation_time >= now) {
    //             upcomingReservations.push(reservations[i]);
    //         } else {
    //             pastReservations.push(reservations[i]);
    //         }
    //     }

    //     return { pastReservations, upcomingReservations };
    // }

    // let upcoming_past_flag = true;

    // function upcoming_past(e) {
    //     upcoming_past_flag = !upcoming_past_flag;
    // }
</script>

<div>
    <Reservations
        dashboard_reservations={"reservations"}
        RESERVATIONS={data.data["reservations"]}
    />
    <!-- Dropdown of "What data to see?" -->
    <!-- <ChooseDate />

    <button
        class="float-right mt-2 mr-2 px-2 outline outline-2"
        on:click={upcoming_past}
    >
        {#if upcoming_past_flag === true}
            Past
        {:else}
            Upcoming
        {/if}
    </button>

    {#if upcoming_past_flag === true}
        <span class="text-3xl font-normal underline"> Upcoming </span>
    {:else}
        <span class="text-3xl font-normal underline"> Past </span>
    {/if}

    <div class="mx-3 mt-3 flex flex-col gap-7 overflow-auto">
        {#if upcoming_past_flag === true}
            {#each $upcomingReservations as reservation}
                <Card {reservation} />
            {/each}
        {:else}
            {#each $pastReservations as reservation}
                <Card {reservation} />
            {/each}
        {/if}
    </div> -->
</div>
