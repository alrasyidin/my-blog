<template>
  <Layout>
    <header class="header">
      <g-image src="~/assets/img/photo.jpg" alt="My Photo" width="100" class="photo" blur="50"></g-image>
      <ul class="navi">
        <li class="navi__li">
          <g-link to="/" class="navi__link link">Home</g-link>
        </li>
        <li class="navi__li">
          <g-link to="/about/" class="navi__link link">About</g-link>
        </li>
      </ul>
      <h1 v-html="$page.metaData.siteName" />
      <p v-html="$page.metaData.siteDescription" />
    </header>
    <section>
      <p>Hallo Semua, perkenalkan saya Hafidh Pradipta Arrasyid. Mahasiswa Teknik Informatika, Universitas Langlangbuana. Calon <strong>Software Engineer</strong> wanna be, doain ya 😎. Saat ini saya sedang menempuh pendidikan S1 dan sekarang lagi menjalankan <strong>Kuliah Kerja Nyata</strong> (selanjutnya disingkat KKN aja ya) yang mana KKN ini merupakan bakti dan pengabdian kepada masyarakat, bangsa dan negara (eehee Indonesia terlalu luas ketang).</p>

      <p>
        Mahasiswa yang selama ini belajar di bangku perkuliahan, belajar, dituntut untuk berbaur, berinteraksi dan bermasyarakat. Melalui pendekatan lintas keilmuan diharapkan mahasiswa dapat mewakafkan ilmu dan menerapkan ke masyarakat. Apa yang telah dipelajari di kampus seyogyanya dapat bermanfaat untuk masyarakat banyak.
      </p>

      <p>
        Kebetulan saya ingin mendokumetasikan dalam bentuk tulisan, sim salabim (dengan keilmuan yang saya miliki, uhu) jadilah blog sederhana ini. Semoga Catatan selama KKN ini bisa kenang-kenangan bahwa kita pernah mengukir sejarah di Desa Cikoneng, Ciparay, Kabupaten Bandung.
      </p>

      <p>
        Ada <i>quote</i> yang menarik yang pengen saya kutip disini 
        <blockquote>"Gantungkan cita-citamu setinggi langit! Bermimpilah setinggi langit. Jika engkau jatuh, engkau akan jatuh di antara bintang-bintang. - Soekarno</blockquote>

        <blockquote>"Gantungkan cita-citamu setinggi langit! Bermimpilah jadi presiden. Jika engkau gagal, minimal engkau jadi menteri lah. - Quote ngasal dari saya</blockquote>
      </p>

      <p>
        Sekian perkenalan dari saya, saya mah orangnya gitu, photo aja malah di blur. Maafin ya! Tujuannya apaaan? biar ada yang kangen.
      </p>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "About"
  }
};
</script>

<page-query>
query {
  metaData {
    siteName
    siteDescription
  }
}

</page-query>

<style>
.header {
  font-family: "Stylish";
  font-size: 20px !important;
  text-align: center;
  line-height: 20px;
  padding: 0.7em;
}

.header p {
  font-weight: 200;
}
.photo {
  border-radius: 50%;
  filter: blur(5px);
}
</style>