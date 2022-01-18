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

<p>Activity: {activity}</p>
<p>Type: {type}</p>
<p>Participants: {participants}</p>



