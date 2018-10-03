<template>
    <div class="timeline">
        <div class="timeline-container timeline-left">
            <div class="timeline-content">
                <img src="../../assets/icon_pendaftaran.svg" class="img-timeline" alt="pendaftaran" />
            </div>
        </div>

        <div class="content-right-unimg">
          <h2>PENDAFTARAN</h2>
          <p>5-25 November 2018</p>
          <p>Penjelasannya gan!</p>
        </div>

        <div class="timeline-container timeline-right">
            <div class="timeline-content">
                <img src="../../assets/icon_penyisihan.svg" class="img-timeline" alt="penyisihan" />
            </div>
        </div>

        <div class="content-left-unimg">
          <h2>BABAK PENYISIHAN</h2>
          <p>26 November 2018 - 19 Januari 2019</p>
          <p>Penjelasannya gan!</p>
        </div>

        <div class="timeline-container timeline-left">
            <div class="timeline-content">
                <img src="../../assets/icon_pengumuman.svg" class="img-timeline" alt="pengumuman" />
            </div>
        </div>

        <div class="content-right-unimg">
          <h2>PENGUMUMAN</h2>
          <p>XX Oktober 2018 - YY Desember 2018</p>
          <p>Penjelasannya gan!</p>
        </div>

        <div class="timeline-container timeline-right">
            <div class="timeline-content">
                <img src="../../assets/icon_final.svg" class="img-timeline" alt="final" />
            </div>
        </div>

        <div class="content-left-unimg">
          <h2>FINAL PRESENTASI</h2>
          <p>XX Oktober 2018 - YY Desember 2018</p>
          <p>Penjelasannya gan!</p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Timeline'
}
</script>
<style>
.content-right-unimg {
  padding: 10px 40px;
  position: relative;
  background-color: inherit;
  width: 150%;
  margin-top: -150px;
  margin-bottom: 50px;
}

.content-left-unimg {
  padding: 10px 40px;
  position: relative;
  background-color: inherit;
  width: 50%;
  margin-top: -130px;
  margin-bottom: 50px;
}

.img-timeline {
  height: 100px;
  width: 100px;
}

.timeline {
  position: relative;
  max-width: 1200px;
  margin: 0 auto;
}

.timeline::after {
  content: '';
  position: absolute;
  width: 6px;
  background-color: brown;
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -3px;
}

.timeline-container {
    padding: 10px 10px;
    position: relative;
    background-color: inherit;
    width: 50%;
}

.timeline-container::after {
  content: '';
  position: absolute;
  width: 25px;
  height: 25px;
  right: -17px;
  background-color: yellow;
  border: 4px solid brown;
  top: 15px;
  border-radius: 50%;
  z-index: 1;
}

.timeline-left {
    left: -4px;
}

.timeline-right {
    left: 50%;
}

.timeline-left::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  right: 30px;
  border: medium solid white;
  border-width: 10px 0 10px 10px;
  border-color: transparent transparent transparent white;
}

.timeline-right::before {
  content: " ";
  height: 0;
  position: absolute;
  top: 22px;
  width: 0;
  z-index: 1;
  left: 30px;
  border: medium solid white;
  border-width: 10px 10px 10px 0;
  border-color: transparent white transparent transparent;
}

.timeline-right::after {
  left: -12px;
}

.timeline-content {
  padding: 20px 30px;
  background-color: white;
  position: relative;
  border-radius: 6px;
}

@media screen and (max-width: 600px) {
/* Place the timelime to the left */
  .timeline::after {
    left: 31px;
  }

/* Full-width containers */
  .timeline-container {
    width: 100%;
    padding-left: 70px;
    padding-right: 25px;
  }

/* Make sure that all arrows are pointing leftwards */
  .timeline-container::before {
    left: 60px;
    border: medium solid white;
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
  }

/* Make sure all circles are at the same spot */
  .timeline-left::after, .timeline-right::after {
    left: 15px;
  }

/* Make all right containers behave like the left ones */
  .timeline-right {
    left: 0%;
  }
}
</style>