<script>
export default {
    data() {
        return {
            quoteList: [
                { quote: 'It just works!', person: 'Me' },
                { quote: 'The greatest glory in living lies not in never falling, but in rising every time we fall.', person: 'Nelson Mandela' },
                { quote: 'The way to get started is to quit talking and begin doing.', person: 'Walt Disney' },
                { quote: "If you look at what you have in life, you'll always have more. If you look at what you don't have in life, you'll never have enough.", person: 'Oprah Winfrey' },
                { quote: "Life is what happens when you're busy making other plans.", person: 'John Lennon' },
                { quote: "Spread love everywhere you go. Let no one ever come to you without leaving happier.", person: "Mother Teresa" },
                { quote: "Always remember that you are absolutely unique. Just like everyone else.", person: "Margaret Mead" },
                { quote: "When you reach the end of your rope, tie a knot in it and hang on.", person: "Franklin D. Roosevelt" },
                { quote: "Don't judge each day by the harvest you reap but by the seeds that you plant.", person: "Robert Louis Stevenson" },
                { quote: "The future belongs to those who believe in the beauty of their dreams.", person: "Eleanor Roosevelt" },
                { quote: "Tell me and I forget. Teach me and I remember. Involve me and I learn.", person: "Benjamin Franklin" },
                { quote: "The best and most beautiful things in the world cannot be seen or even touched — they must be felt with the heart.", person: "Helen Keller" },
                { quote: "It is during our darkest moments that we must focus to see the light.", person: "Aristotle" },
                { quote: "Whoever is happy will make others happy too.", person: "Anne Frank" },
                { quote: "Do not go where the path may lead, go instead where there is no path and leave a trail.", person: "Ralph Waldo Emerson" },
                { quote: "You will face many defeats in life, but never let yourself be defeated.", person: "Maya Angelou" },
                { quote: "Many of life's failures are people who did not realize how close they were to success when they gave up.", person: "Thomas A. Edison" },
                { quote: "Life is a long lesson in humility.", person: "James M. Barrie" },
                { quote: "Love the life you live. Live the life you love.", person: "Bob Marley" },
                { quote: "Success is not final; failure is not fatal: It is the courage to continue that counts.", person: "Winston S. Churchill" },
                { quote: "You miss 100% of the shots you don't take.", person: "Wayne Gretzky" },
                { quote: "Whether you think you can or you think you can't, you're right.", person: "Henry Ford" },
                { quote: "I alone cannot change the world, but I can cast a stone across the water to create many ripples.", person: "Mother Teresa" },
                { quote: "The only person you are destined to become is the person you decide to be.", person: "Ralph Waldo Emerson" },
                { quote: "True terror is to wake up one morning and discover that your high school class is running the country.", person: "Kurt Vonnegut" },
                { quote: "Always forgive your enemies; nothing annoys them so much.", person: "Oscar Wilde" },
                { quote: "Sometimes the road less traveled is less traveled for a reason.", person: "Jerry Seinfeld" },
                { quote: "If you want to know what God thinks of money, just look at the people he gave it to.", person: "Dorothy Parker" },
                { quote: "When in doubt, look intelligent.", person: "Garrison Keillor" },
                { quote: "I'm the man who'll be king of the pirates!", person: "Monkey D. Luffy"},
                { quote: "Yare Yare Daze", person: "Jotaro Kujo"},
                { quote: "If you are not yelling at your kids, you are not spending enough time with them.", person: "Reese Witherspoon" },
                { quote: "The older you get the more you realize that kindness is synonymous with happiness.", person: "Lionel Barrymore" },
                { quote: "Happiness makes up in height for what it lacks in length.", person: "Robert Frost" },
                { quote: "The best way to predict the future is to create it.", person: "Peter F. Drucker" },
                { quote: "I'll make you 15.000.000 children.", person: "Sasavi Momak" },
                { quote: "Boy.", person: "Kratos"},
                { quote: "A problem is a chance for you to do your best.", person: "Duke Ellington"},
                { quote: "Time you enjoy wasting was not wasted.", person: "John Lennon" },
                { quote: "The tallest mountains started as a stone.", person: "Jonathan Young" },
                { quote: "Don't be afraid to be afraid.", person: "Maurice Chevalier" },
                { quote: "A brave man acknowledges the strength of others", person: "Veronica Roth" },
                { quote: "Scared is what you're feeling. Brave is what you're doing.", person: "Emma Donoghue" },
                { quote: "To know sorrow is not terrifying. What is terrifying is to know you can't go back to happiness you could have.", person: "Matsumoto Rangiku" },
                { quote: "Power comes in response to a need, not a desire, you have to create that need.", person: "Goku" },
                { quote: "If you don't take risks, you can't create a future!" , person: "Monkey D. Luffy" },
                { quote: "If you don't share someone's pain, you can never understand them.", person: "Nagato" },
                { quote: "I'll leave tomorrow's problems to tomorrow's me.", person: "Saitama" },
                { quote: "If you can't do something, then don't. Focus on what you can.", person: "Shiroe" },
                { quote: "You can die anytime, but living takes true courage.", person: "Kenshin Himura" },
                { quote: "Being weak is nothing to be ashamed of… Staying weak is!!", person: "Fuegoleon Vermillion" },
                { quote: "My magic is never giving up!!!!", person: "Asta" },
                { quote: "A dropout will beat a genius through hard work.", person: "Rock Lee" },
                { quote: "Reject common sense to make the impossible possible.", person: "Simon" },
                { quote: "If you really want to be strong… Stop caring about what your surrounding thinks of you!", person: "Saitama" },
                { quote: "Hard work is worthless for those that don't believe in themselves.", person: "Naruto Uzumaki" },
                { quote: "If you just submit yourself to fate, then that's the end of it.", person: "Keiichi Maebara" },
                { quote: "We can't waste time worrying about the what if's.", person: "Ichigo Kurosaki" },
                { quote: "Fools who don't respect the past are likely to repeat it.", person: "Nico Robin" },
                { quote: "The world isn't perfect, but it's there for us, doing the best it can… that's what makes it so damn beautiful.", person: "Roy Mustang" },
                { quote: "You need to accept the fact that you're not the best and have all the will to strive to be better than anyone you face.", person: "Roronoa Zoro" },
                { quote: "Death can have me, when it earns me!", person: "Kratos" }
            ],
            quote: '',
            person: ''
        };
    },
    mounted() {
        window.addEventListener('load', () => {
            this.getQuote();
        }, {once: true})
    },
    methods: {
        getQuote() {
            const index = Math.floor(Math.random() * this.quoteList.length);
            const member = this.quoteList[index];

            this.quote = member.quote;
            this.person = member.person;
        }
    }
}
</script>

<template>
    <p class="quote">" {{quote}} "</p>
    <p class="person">- {{person}}</p>
    <button class="quote-btn" @click="getQuote">Next Quote</button>
</template>

<style scoped>
    p {
        color: white;
        text-align: start;
        font-size: 3rem;
        transition: all .7s;
    }

    .quote {
        padding: 3rem 3rem .5rem 3rem;
    }

    .person {
        padding: .5rem 3rem 3rem 3rem;
        transform: translateX(70%);
    }

    .quote-btn {
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translate(-50%, 150%);
        font-size: 3rem;
        border-radius: .5rem;
        outline: none;
        border: .3rem solid black;
        box-shadow: 3px 3px 3px black;
        cursor: pointer;
    }

    .quote-btn:active {
        box-shadow: -3px -3px 3px black;
    }
</style>