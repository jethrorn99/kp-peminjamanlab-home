<template>
    <div class="row">
      <div class="col-12">
        <card :title="table1.title" :subTitle="table1.subTitle">
          <div slot="raw-content" class="table-responsive">
            <paper-table :data="table1.data" :columns="table1.columns">

            </paper-table>
          </div>
        </card>
      </div>

      <div class="col-12">
        <card class="card-plain">
          <div class="table-full-width table-responsive">
            <paper-table type="hover" :title="table2.title" :sub-title="table2.subTitle" :data="table2.data"
                         :columns="table2.columns">

            </paper-table>
          </div>
        </card>
      </div>

    </div>
</template>
<script>
import { PaperTable } from "@/components";
const tableColumns = ["Id", "Nama", "NIM", "Ruangan", "Alasan"];
const tableData = [
  {
    id: 1,
    nama: "Jeketi Palapan",
    nim: "1710511041",
    ruangan: "FIKLAB401",
    alasan: "Kelas"
  },
];

export default {
  components: {
    PaperTable
  },
  data() {
    return {
      table1: {
        title: "Tabel 1",
        subTitle: "Request",
        columns: [...tableColumns],
        data: [...tableData]
      },
      table2: {
        title: "Tabel User",
        subTitle: "Verifikasi User",
        columns: [...tableColumns],
        data: [...tableData]
      }
    };
  }
};
</script>
<style>
</style>
