<template>
    <div class="nfts-list">
        <div v-for="nft in nfts" :key="nft.token_id"> 
            <SingleNFT :nft="nft" />
        </div>
    </div>
</template>

<script>
import SingleNFT from './SingleNFT.vue'

export default {
    name: 'NftsList',
    props: {
        nfts: Array
    },
    components: {
        SingleNFT
    }
}
</script>

<style scoped>
    .nfts-list {
        padding: 0px 40px;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: 1fr;
        gap: 20px 40px;
        width: 80%;
        margin: auto;
    }
    
    @media (max-width: 950px) {
        .nfts-list {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    @media screen and (max-width: 650px) {
        .nfts-list {
            grid-template-columns: 1fr;
        }

        
    }
</style>
