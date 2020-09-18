<template>
    <div>
        <button @click="layoutChange" id="change">View</button>
        <h1>List of Tweets</h1>
        <div id="tweets-container" :class="{tweetsGrid: isGrid}">
            <div class="tweets" v-for="tweet in tweets" v-bind:key="tweet">
                <h3 class="tweet-username">{{ tweet.username }}</h3>
                <h3 class="tweet-date">{{ tweet.date }}</h3>
                <p class="tweet-content">{{ tweet.content }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "page-tweet",
    methods: {
        layoutChange: function() {
            if(this.isGrid == true) {
                this.isGrid = false;
                document.getElementById("change").innerHTML = "Change to grid View";
            } else if(this.isGrid == false) {
                this.isGrid = true;
                document.getElementById("change").innerHTML = "Change to list View";
            }
        }
    },
    data: function() {
        return {
            tweets: [
            {content: "Alberta chief medical officer to update COVID-19 reponse Thursday", 
            username: "Globalnews",
            date: "08-18-2020",
            }, 
            {content: "Calgary brewery resurrects more than century-old beverage Cronk", 
            username: "Globalnews",
            date: "08-18-2020",
            }, 
            {content: "Popular Calgary obstacle course center InjaNation set to close", 
            username: "Globalnews",
            date: "08-19-2020",
            }, 
            {content: "There is no longer a heat warning in place for Calgary", 
            username: "Globalnews",
            date: "08-19-2020",
            }, 
            {content: "Calgary couple arrested, drugs and guns seized", 
            username: "Globalnews",
            date: "08-19-2020",
            }, 
            {content: "Massive smoke plumes rising from wildfire burining south of Penticton", 
            username: "Globalnews",
            date: "08-20-2020",
            }, 
            {content: "Trudeau planning social welfare system overhaul", 
            username: "Globalnews",
            date: "08-20-2020",
            }, 
            {content: "Fire investigator probes cause of northwest Calgary house fire", 
            username: "Globalnews",
            date: "08-18-2020",
            }, 
            {content: "Solar project seeks to replace abandoned oil wells in rural Alberta", 
            username: "Globalnews",
            date: "08-20-2020",
            }, 
            {content: "What to know about the CRA breach and shutdown", 
            username: "Globalnews",
            date: "08-20-2020",
            }
            ],
            isGrid: true,
        }
    }


}

</script>

<style scoped>
    .tweetsGrid {
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: repeat(3, 1fr);
    }
</style>