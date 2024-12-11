<template>
    <div class="nft-details-container">
        <div class="nft-img-holder">
            <img class="nft-image" :src="nft.image" />
        </div>
        <h2 class="nft-collection-name">{{ nft.collectionName }}</h2>
        <h2 class="nft-title">{{ nft.nftName }}</h2>
        <p class="nft-author-info">Creator: {{ nft.creatorName }}</p>
        <p class="nft-owner">Owner: {{ nft.ownerName }} </p>
        <p class="nft-price">Price: ${{ nft.price }}</p>

        <p class="nft-last-sale-price">Last Sale Price: {{ nft.lastSalePrice }} ETH</p>
        <p class="nft-sale-date">Date of Sale: {{ nft.dateOfSale }}</p>
        
        <div class="nft-tags">
            <p class="nft-token-id">Token ID: {{ nft.tokenId }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SingleNFT',
    props: {
        nft: Object
    }
}
</script>

<style scoped>
.nft-details-container {
    padding: 20px;
    background-color: white;
    line-height: 1.5rem;
    border-radius: 8px;
    margin-bottom: 1rem;
    /* background-color: #ff6b22; */
    background-color: #CCFF00;

    color: #FFF;
    transition: all 0.3s ease; 
}
.nft-collection-name {
    text-align: center;
    margin: 0.5rem 0;
    color: #FFD700;
    /* color: coral; */
    /* color: #154406; */
color: #033500;
    font-size: 1.2rem;
    text-transform: capitalize;


}

.nft-title {
    text-align: center;
    margin: 0.5rem 0;
    text-transform: uppercase;
    color: rgb(17, 15, 12);
    font-size: 1.3rem;
}

.nft-author-info,.nft-owner {
    text-align: right;
    font-size: 0.8rem;
    color: #2C2C2C;
    font-weight: bold;
    justify-content: end;

}

.nft-price, .nft-last-sale-price, .nft-sale-date {
    font-size: 0.85rem;
    text-align: justify;
    margin: 0.5rem 0;
    color: #3E2723
}

.nft-img-holder {
    width: 100%;
    text-align: center;
}
.nft-image {
    width: 100%;
    max-height: 425px;
    object-fit: cover;
    border-radius: 8px;
    border: 2px solid #1c1818;
}

.nft-tags {
    display: flex;
    justify-content: space-around;
    margin: 0.5rem 0;
}

.nft-token-id {
    color: #000;
    background-color: #FFF;
    padding: 5px 10px;
    border-radius: 10px;
    font-size: 0.8rem;
    letter-spacing: 1px;
    font-weight: bold;
}
@media screen and (max-width: 1400px) {
    .nft-img-container {
        width: 100%;
    }
    .nft-image {
        width: 100%;
        max-height: 400px;
    }
    .nft-collection-name{
        height: 3rem;

    }
    .nft-title{
        font-size: 1.5rem;
    }
    .nft-creator-name .nft-author-info{
        font-size: 1rem;
    }
    
}

@media screen and (max-width: 1050px) {
    .nft-img-container {
        width: 100%;
    }
    .nft-image {
        width: 100%;
        max-height: 300px;
    }
    .nft-collection-name{
        height: 3rem;

    }
    .nft-title{
        font-size: 1rem;
    }
    .nft-author-info{
        font-size: 0.7rem;
    }
    
}

</style>
