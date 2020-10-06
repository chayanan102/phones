<template>
  <v-container>
    <v-flex class="text-center">
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935878267568149/1plus.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935883040292874/apple.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935883715706890/ASUS.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935885863714836/nokia.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935886123761664/huawei.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935887343910912/oppo.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935889055449128/pixel.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935890376916992/realme.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935892046118932/samsung.png"  height="90" width="90"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762935893702606848/sony.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762936137077358602/xiaomi.png"  height="80" width="80"/>
        <img src="https://cdn.discordapp.com/attachments/762935827121700874/762936140994445342/vivo.png"  height="80" width="80"/>
        

    </v-flex>
  <!-- แบบฟอร์มกรอกข้อมูล -->
    <!-- ชนิดโทรศัพท์ -->
    <v-container fluid>
        <v-row align="center">
            <v-col
            class="d-flex"
            cols="12"
            sm="12"
            required
        >
        <v-select
          :items="items"
          label="Mobile Phone Brand"
          filled
        ></v-select>
            </v-col>  
        </v-row>
  </v-container>

   <v-form v-model="valid">
    <v-container>
      <v-row>
        <!-- ไซส์หน้าจอ -->
        <v-col cols="12" md="4">
          <v-text-field
            v-model="ScreenSize"
            :rules="nameRules"
            label="Screen Size(inch)"
            required
          ></v-text-field>
        </v-col>

        <!-- ชิป -->
        <v-col cols="12" md="8">
          <v-text-field
            v-model="Chip"
            :rules="nameRules"
            label="Chip"
            required
          ></v-text-field>
        </v-col>

        <!-- หน้าจอ -->
        <v-col cols="12" md="6">
          <v-text-field
            v-model="Display"
            :rules="nameRules"
            label="Display"
            required
          ></v-text-field>
        </v-col>

        <!-- ความจุ -->
        <v-col cols="12" md="6">
          <v-text-field
            v-model="Memory"
            :rules="nameRules"
            label="Memory"
            required
          ></v-text-field>
        </v-col>

        <!-- กล้องหน้า -->
        <v-col cols="12" md="6">
          <v-text-field
            v-model="FrontCamera"
            :rules="nameRules"
            label="Front Camera(MP)"
            required
          ></v-text-field>
        </v-col>

        <!-- กล้องหลัง -->
        <v-col cols="12" md="6">
          <v-text-field
            v-model="BackCamera"
            :rules="nameRules"
            label="Back Camera(MP)"
            required
          ></v-text-field>
        </v-col>

        <!-- พอร์ตเชื่อมต่อ -->
        <v-col cols="12" md="2">
          <v-text-field
            v-model="ConnectionPorts"
            :rules="nameRules"
            label="Connection Ports"
            required
          ></v-text-field>
        </v-col>

        <!-- ซิมการ์ด -->
        <v-col cols="12" md="5">
          <v-text-field
            v-model="SimCard"
            :rules="nameRules"
            label="Sim Card"
            required
          ></v-text-field>
        </v-col>

        <!-- กันน้ำ -->
        <v-col cols="12" md="5">
          <v-text-field
            v-model="WaterResistant"
            :rules="nameRules"
            label="Water Resistant"
            required
          ></v-text-field>
        </v-col>

        <!-- การชาร์จแบบไร้สาย -->
        <v-col cols="12" md="6">
          <v-text-field
            v-model="WirelessCharging"
            :rules="nameRules"
            label="Wireless Charging"
            required
          ></v-text-field>
        </v-col>

        <!-- อายุแบตเตอรี่ -->
        <v-col cols="12" md="6">
          <v-text-field
            v-model="BatteryLife"
            :rules="nameRules"
            label="Battery Life"
            required
          ></v-text-field>
        </v-col>

        <!-- ระบบปฏิบัติการ -->
        <v-col cols="12" md="3">
          <v-text-field
            v-model="OperatingSystem"
            :rules="nameRules"
            label="Operating System"
            required
          ></v-text-field>
        </v-col>

        <!-- สี -->
        <v-col cols="12" md="3">
          <v-text-field
            v-model="Color"
            :rules="nameRules"
            label="Color"
            required
          ></v-text-field>
        </v-col>

        <!-- ความปลอดภัย -->
        <v-col cols="12" md="6">
          <v-text-field
            v-model="Security"
            :rules="nameRules"
            label="Security"
            required
          ></v-text-field>
        </v-col>        

        <!-- ขนาดกว้าง x ลึก x สูง -->
        <v-col cols="12" md="6">
          <v-text-field
            v-model="Dimensions"
            :rules="nameRules"
            label="Dimensions W x D x H(cm.)"
            required
          ></v-text-field>
        </v-col>

        <!-- น้ำหนัก -->
        <v-col cols="12" md="3">
          <v-text-field
            v-model="Weight"
            :rules="nameRules"
            label="Weight(Kg.)"
            required
          ></v-text-field>
        </v-col>

        <!-- ประกัน -->
        <v-col cols="12" md="3">
          <v-text-field
            v-model="Warranty"
            :rules="nameRules"
            label="Warranty(Year)	"
            required
          ></v-text-field>
        </v-col>

        <!-- การชาร์จ -->
        <v-col cols="12" md="7">
          <v-text-field
            v-model="Charging"
            :rules="nameRules"
            label="Charging"
            required
          ></v-text-field>
        </v-col>

        <!-- แบตเตอรี่ -->
        <v-col cols="12" md="5">
          <v-text-field
            v-model="Battery"
            :rules="nameRules"            
            label="Battery(mAh)"
            required
          ></v-text-field>
        </v-col>
        
        <!-- Network -->
        <v-col cols="12" md="5">
          <v-text-field
            v-model="Network"
            :rules="nameRules"            
            label="Network"
            required
          ></v-text-field>
        </v-col>        
        
        <!-- หน่วยความจำและซิมการ์ดที่ขยายได้ -->
        <v-col cols="12" md="5">
          <v-text-field
            v-model="upmemory"
            :rules="nameRules"            
            label="Expandable Memory and Sim Card"
            required
          ></v-text-field>
        </v-col>

        <!-- ราคา -->
        <v-col cols="12" md="2">
          <v-text-field
            v-model="Price"
            :rules="nameRules"            
            label="Price(Baht)"
            required
          ></v-text-field>
        </v-col>
        
        <!-- submit -->
        <v-container fluid>
          <v-btn
            class="mr-4"
            @click="submit"
          >
            submit
          </v-btn>
        </v-container>

      </v-row>
    </v-container>
  </v-form>
    
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      valid: false,
      ScreenSize: '',
      Chip: '',
      Display: '',
      Memory: '',
      FrontCamera: '',
      BackCamera: '',
      ConnectionPorts: '',
      SimCard:'',
      WaterResistant:'',
      WirelessCharging:'',
      BatteryLife:'',
      OperatingSystem:'',	
      Color:'',
      Security:'',
      Dimensions:'',
      Weight:'',
      Warranty:'',
      Charging:'',
      Battery:'',
      Network:'',
      upmemory:'',
      Price:'',
      items: ['Oneplus', 'Huawei', 'Nokia', 'Oppo','Samsung','Vivo','Xiaomi','Apple','Realme','Sony','Asus','Pixel'],

      nameRules: [
        v => !!v || 'Required',     
      ],
            
    }),
      methods: {
      submit () {
        this.$v.$touch()
      },
     }
  }
</script>

<style>
.theme--dark.v-application {
  font-family: 'Sarala', sans-serif;
  background-image: url('https://images.wallpaperscraft.com/image/green_gray_color_153734_1920x1080.jpg');
  background-attachment: fixed;
  background-position: 100% 100%;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>


