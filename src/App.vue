<template>
  <div class="container">
    <h1 class="title">Consistency, Integrity, Innovation</h1>
    <div class="cards">
      <div v-for="(card, index) in cards" :key="index" class="card">
        <div class="glass-effect">
          <div class="icon-container">
            <img :src="card.icon" alt="Icon" class="icon" />
          </div>
          <p class="card-title">{{ card.title }}</p>
          <a :href="card.link" target="_blank">
            <button class="btn">Learn More</button>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        { title: "Green IT Ltd.", icon: require('@/assets/images/green_it_logo.png'), link: 'https://greenitmm.com/' },
        { title: "Globe Trading Ltd.", icon: require('@/assets/images/globe_logo.png'), link: "https://globe.update.itgateway.cloud/" },
        { title: "Green IT Pte Ltd", icon: require('@/assets/images/green_it_logo.png'), link: "https://greenit-sg.com/" },
      ]
    };
  }
};
</script>

<style scoped>
body {
  font-family: 'Poppins', sans-serif;
  margin: 0;
  overflow: hidden;
}

.container {
  background: url('@/assets/images/bg_3.jpg') no-repeat center center/cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
  height: 100vh;
  width: 100vw;
  position: fixed;
}

.title {
  font-family: Montserrat, sans-serif;
  font-size: 1.8em;
  font-weight: 700;
  margin-bottom: 40px;
  text-shadow: 3px 3px 12px rgba(0, 0, 0, 0.4);
  letter-spacing: 1.5px;
  padding: 20px 40px;
  background: linear-gradient(189deg, rgb(26 63 139 / 60%), hsla(0, 0%, 100%, 0.1));
  border-radius: 30px;
  display: inline-block;
  backdrop-filter: blur(12px);
  border: 2px solid rgba(255, 255, 255, 0.3);
  color: #40c534;
}

.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 50px;
  width: 100%;
  max-width: 1200px;
  margin-top: 50px;
}

.card {
  width: 150px;
  padding: 20px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(20px);
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
  border: 1px solid rgba(255, 255, 255, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0px 0px 30px rgba(255, 255, 255, 0.4);
}

.icon-container {
  width: 120px;
  height: 120px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: white;
  border-radius: 50%;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
  margin: 0 auto 15px;
}

.icon {
  width: 100px;
  height: auto;
}

.card-title {
  font-size: 1.2em;
  font-weight: 700;
  margin-bottom: 10px;
  color: white;
}

.btn {
  margin-top: 10px;
  background: linear-gradient(189deg, rgb(26 63 139 / 60%), hsla(0, 0%, 100%, 0.1));
  color: #40c534;
  padding: 10px 15px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn:hover {
  background: rgba(255, 255, 255, 0.3);
}

/* Responsive Styles */
@media (max-width: 768px) {
  .cards {
    flex-direction: column;
    align-items: center;
  }
  
  .card {
    width: 90%;
    max-width: 300px;
  }
}
</style>
