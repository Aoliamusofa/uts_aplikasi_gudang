<template>
  <div>
    <div class="container mx-auto">
      <p class="font-semibold text-center mt-2 mb-5">Detail kategori</p>
      <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
        <table class="w-full text-sm text-left text-slate-500">
          <thead class="bg-slate-100 text-xs border-b text-slate-700 uppercase hover:bg-slate-50 text-center">
            <tr>
              <th scope="col" class="px-6 py-4">ID Kategori</th>
              <th scope="col" class="px-6 py-4">Nama Kategori</th>
              <th scope="col" class="px-6 py-4">Keterangan</th>
            </tr>
          </thead>
          <tbody id="example">
            <tr data_kategori :key="data_kategori.kategoriId" class="bg-white border-b hover:bg-slate-100 text-center">
              <td class="px-6 py-4">{{ data_kategori.kategoriId }}</td>
              <td class="px-6 py-4">{{ data_kategori.kategori }}</td>
              <td class="px-6 py-4">{{ data_kategori.keterangan }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>
<script>
import axios from "axios";
const BaseUrl = "https://664307293c01a059ea212f61.mockapi.io/api/v1";
definePageMeta({ layout: false });
export default {
  data() {
    return {
      kategoriId: "",
      data_kategori: {},
    };
  },
  mounted() {
    this.kategoriId = this.$route.params.id;
    this.GetDataKategori(this.kategoriId);
  },
  methods: {
    GetDataKategori(kategoriId) {
      axios.get(BaseUrl + `/kategori/${kategoriId}`).then((res) => {
        this.data_kategori = res.data; //ambil semua data dosen yang mengampu satu matakuliah berdasarkan id yang di kirim dari URL
        // this.kategoriId = kategoriId; //ambil id matakuliah dari URL lalu tampung ke variabel kategoriId
      });
    }
  },
};
</script>
<style lang="scss" scoped></style>
