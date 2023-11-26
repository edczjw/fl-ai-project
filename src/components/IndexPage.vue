<script setup lang="ts"> 
import { loadFull } from "tsparticles";
 
const options = {
    // background: {
    //     color: {
    //         value: '#fff'
    //     }
    // },
    fpsLimit: 120,
    interactivity: {
        events: {
            onClick: {
                enable: true,
                mode: 'push'
            },
            onHover: {
                enable: true,
                mode: 'repulse'
            },
            resize: true
        },
        modes: {
            bubble: {
                distance: 400,
                duration: 1,
                opacity: 0.8,
                size: 10
            },
            push: {
                quantity: 4
            },
            repulse: {
                distance: 200,
                duration: 0.4
            }
        }
    },
    particles: {
        color: {
            value: '#ffffff'
        },
        links: {
            color: '#ffffff',
            distance: 150,
            enable: true,
            opacity: 0.2,
            width: 0.2
        },
        collisions: {
            enable: true
        },
        move: {
            direction: 'none',
            enable: true,
            outModes: {
                default: 'bounce'
            },
            random: false,
            speed: 2,
            straight: false
        },
        number: {
            density: {
                enable: true,
                area: 800
            },
            value: 80
        },
        opacity: {
            value: 0.2
        },
        shape: {
            type: 'circle'
        },
        size: {
            value: { min: 1, max: 5 },
        }
    },
    detectRetina: true
 
}
const particlesInit = async (engine: any) => {
    await loadFull(engine);
};
 
const particlesLoaded = async (container: any) => {
    console.log("Particles container loaded", container);
}; 
 
</script>

<template>
  <div class="first-page flex">
    <div class="header">
      <div class="inner-header">
        <div class="flex">
          <h1>专业法律工作者的AI生产力工具</h1>
        </div>
        <h4>消灭90%以上的基础法律工作时间，让您的时间花在最有价值的地方</h4>
      </div>
    </div> 
    <Particles id="tsparticles" :particlesInit="particlesInit" :particlesLoaded="particlesLoaded" :options="options" />

    <div class="content flex">
      <RouterLink to="/contact" class="brk-btn btn-11"
        >开始试用
        <div class="dot"></div
      ></RouterLink>
    </div>
  </div>
</template>

<style scoped lang="scss">
.first-page {
  border: 1px solid #000;
  height: 100vh;
  background: url(../assets/images/background.jpg) center no-repeat;
  background-size: 100% 100%;
  position: relative;
} 
.content{
  position: absolute;
  bottom: 30px;
  border: 1px solid #000; 
}
h1 {
  font-family: 'Lato', sans-serif;
  font-weight: 500;
  letter-spacing: 2px;
  font-size: 52px;
}
h4 {
  font-family: 'Lato', sans-serif;
  font-weight: 300;
  letter-spacing: 2px;
  font-size: 26px;
  line-height: 64px;
}
.header {
  position: relative;
  text-align: center;
  color: white;
}
.logo {
  width: 50px;
  fill: white;
  padding-right: 15px;
  display: inline-block;
  vertical-align: middle;
}

.inner-header {
  height: 65vh;
  width: 100%;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.brk-btn {
  width: 130px;
  height: 40px;
  line-height: 40px;
  color: #fff;
  border-radius: 5px;
  font-family: 'Lato', sans-serif;
  font-weight: 500;
  background: transparent;
  cursor: pointer;
  transition: all 0.3s ease;
  position: relative;
  display: inline-block;
  text-align: center;
  box-shadow: inset 2px 2px 2px 0px rgba(255, 255, 255, 0.5), 7px 7px 20px 0px rgba(0, 0, 0, 0.1),
    4px 4px 5px 0px rgba(0, 0, 0, 0.1);
}
/* 11 */
.btn-11 {
  border: none;
  background: #00faca;
  background: linear-gradient(0deg, #0c655287 0%, #1ceec4 100%);
  color: #fff;
  overflow: hidden;
}
.btn-11:hover {
  text-decoration: none;
  color: #fff;
  font-weight: 600;
}
.btn-11:before {
  position: absolute;
  content: '';
  display: inline-block;
  top: -180px;
  left: 0;
  width: 30px;
  height: 100%;
  background-color: #fff;
  animation: shiny-btn1 3s ease-in-out infinite;
}
.btn-11:hover {
  opacity: 0.9;
}
.btn-11:active {
  box-shadow: 4px 4px 6px 0 rgba(255, 255, 255, 0.3), -4px -4px 6px 0 rgba(116, 125, 136, 0.2),
    inset -4px -4px 6px 0 rgba(255, 255, 255, 0.2), inset 4px 4px 6px 0 rgba(0, 0, 0, 0.2);
}

@keyframes shiny-btn1 {
  0% {
    -webkit-transform: scale(0) rotate(45deg);
    opacity: 0;
  }
  80% {
    -webkit-transform: scale(0) rotate(45deg);
    opacity: 0.5;
  }
  81% {
    -webkit-transform: scale(4) rotate(45deg);
    opacity: 1;
  }
  100% {
    -webkit-transform: scale(50) rotate(45deg);
    opacity: 0;
  }
}

.flex {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
