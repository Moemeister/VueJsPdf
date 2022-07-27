<template>
  <div id="app">
    <button @click="exportPdf" >Descargar</button>
  </div>
</template>
<script>
import jsPDF from "jspdf";
import 'jspdf-autotable';
export default {

  data() {
    return {
      arr: [
        {
          "id": 1,
          "placa": "p123",
          "viajes": [
            {
              "origen": "origen1",
              "destino": "destino1",
              "paradas": [
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },

              ]
            },
            {
              "origen": "origen2",
              "destino": "destino2",
              "paradas": null
            }
          ]
        },
        {
          "id": 2,
          "placa": "p456",
          "viajes": [
            {
              "origen": "origen1",
              "destino": "destino1",
              "paradas": [
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
                {
                  "id": 1,
                  "nombre_parada": "parada1"
                },
                {
                  "id": 2,
                  "nombre_parada": "parada2"
                },
                {
                  "id": 3,
                  "nombre_parada": "parada3"
                },
                {
                  "id": 4,
                  "nombre_parada": "parada4"
                },
                {
                  "id": 5,
                  "nombre_parada": "parada5"
                },
              ]
            },
            {
              "origen": "origen2",
              "destino": "destino2",
              "paradas": null
            }
          ]
        }
      ],
      viaje: [],
      viajes: [],
    }
  },
  methods: {
    exportPdf () {
      const imgData = 'data:image/png;base64,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';
      this.viajes = this.arr.map((element) => {
        return element.viajes.reduce((prev, el) => {
          if(el.paradas === null){
            return [...prev, {
              placa: element.placa,
              origen:  el.origen,
              destino: el.destino
            }]
          }
          return [...prev, {
            placa: element.placa,
            origen: el.origen
          }, ...el.paradas.map( (parada)=> {
            return {
              placa: element.placa,
              destino: parada.nombre_parada
            }
          }), {placa: element.placa, destino: el.destino}
          ]
        }, [])

      })

      var columns = [
        {title: "Origen", dataKey: "origen"},
        {title: "Destino", dataKey: "destino"}
      ];
      var doc = new jsPDF('l', 'pt', 'letter');
      var pageWidth = doc.internal.pageSize.width || doc.internal.pageSize.getWidth();


      // console.log(totalPages)
      // doc.html("<div style='width: 100vw; height: 20px; margin-top: 10px; background-color:red;' ></div>", {

      console.log(this.viajes)
      this.viajes.forEach((el, index, arr) => {
        console.log(el[index].placa)
        doc.autoTable(columns, el, {
          margin: { top: 80 },
          theme: 'grid',
          didDrawPage: function (data) {

            // Header
            doc.setFontSize(10);
            doc.setTextColor(40);
            doc.addImage(imgData, 'png', pageWidth / 2, 30, 50, 50);
            doc.text(el[index].placa,pageWidth / 2 , 22, {align: "center"});

            // Footer
            var str = "Page " + doc.internal.getNumberOfPages();
            doc.setFontSize(10);

            // jsPDF 1.4+ uses getWidth, <1.4 uses .width
            var pageSize = doc.internal.pageSize;
            var pageHeight = pageSize.height
                ? pageSize.height
                : pageSize.getHeight();
            doc.text(str, data.settings.margin.left, pageHeight - 10);
          }
        });
        if(index < arr.length -1){
          doc.addPage()
        }
        doc.html("<table style='border: 1px solid black; border-collapse: collapse;'>" +
            "<td>el</td>" +
            "" +
            "</table>", {
          x: 30,
          y: 30,
          html2canvas: {
            scale: (doc.internal.pageSize.width - 10 * 2 ) / document.body.scrollWidth
          },

        });

      })


      const totalPages = doc.internal.getNumberOfPages()
      console.log(totalPages)

      for (let i = 1; i <= totalPages; i++) {

        doc.setPage(i)

        doc.setFontSize(10)
        doc.setTextColor(150)
        doc.text('Page ' + i + ' of ' + totalPages, (doc.internal.pageSize.getWidth() * 0.88), (doc.internal.pageSize.getHeight() - 0.3))
      }
      doc.save()
    }
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
