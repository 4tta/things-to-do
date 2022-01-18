<script>
    let activity="";
    let type="";
    let participants="";
    
    async function getInfo() {
        fetch('https://www.boredapi.com/api/activity')
            .then((response) => response.json())
            .then((data) => {
                activity = data.activity;
                type = data.type;
                participants = data.participants;

            });
    }
</script>



<div class="p-3">
    <h1>Thing To Do</h1>

    <p>Activity: {activity}</p>
    <p>Type: {type}</p>
    <p>Participants: {participants}</p>

    <form on:submit|preventDefault={getInfo}>
        <button type="submit" class="btn btn-success">Check</button>
    </form>
</div>




