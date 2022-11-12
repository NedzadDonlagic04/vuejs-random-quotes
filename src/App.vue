<template>
    <div class="quote-container">
        <p class="quote">"It simply works"</p>
        <p class="person">- Me</p>
    </div>
</template>

<style scoped>
    .quote-container {
        height: 15rem;
        width: 100rem;
        background-color: var(--bg-cover);
        color: white;
        font-size: 3rem;
        position: relative;
    }

    .quote {
        position: absolute;
        top: var(--vertical-pos);
        left: var(--horizontal-pos1);
        padding: 3rem 3rem .5rem 3rem;
        transform: translateX(-5rem);
    }

    .person {
        position: absolute;
        bottom: var(--vertical-pos);
        right: var(--horizontal-pos1);
        padding: .5rem 3rem 3rem 3rem;
        transform: translateX(5rem);
    }

    .quote,
    .person {
        opacity: 0;
        transition: all var(--quote-animation-time);
    }

    .quote-container:hover .quote,
    .quote-container:hover .person{
        opacity: 1;
    }

    .quote-container:hover .quote {
        left: var(--horizontal-pos2);
    }

    .quote-container:hover .person {
        right: var(--horizontal-pos2);
    }
</style>