<template>
  <div>
    <v-app-bar app flat>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <v-btn icon class="mr-5">
        <v-icon>mdi-bell-outline</v-icon>
      </v-btn>
      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-avatar size="35" v-bind="attrs" v-on="on">
            <v-icon>mdi-account-circle</v-icon>
          </v-avatar>
        </template>
        <v-list class="py-0" dense>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account-circle</v-icon>
            </v-list-item-icon>
            <v-list-item-title>الملف الشخصى</v-list-item-title>
          </v-list-item>
          <v-divider></v-divider>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-logout</v-icon>
            </v-list-item-icon>
            <v-list-item-title>تسجيل الخروج</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
    <v-navigation-drawer right fixed app v-model="drawer">
      <v-list-item style="height: 64px">
        <v-list-item-content>
          <v-list-item-title class="text-h6 primary--text">
            ELSYSTM
          </v-list-item-title>
          <v-list-item-subtitle>2022-2023</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
      <v-divider></v-divider>
      <v-list nav dense>
        <v-list-item link to="/">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>الرئيسية</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link to="/settings">
          <v-list-item-icon>
            <v-icon>mdi-cog</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>الإعدادات الرئيسية</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-subheader>معهد إدارة</v-subheader>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-calculator-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الحسابات</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-school</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون الطلاب</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-account-group</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون العاملين</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-book-open-page-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>التعليم الألكترونى</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-subheader>معهد هندسة</v-subheader>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-calculator-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الحسابات</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-school</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون الطلاب</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-account-group</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون العاملين</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-book-open-page-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>التعليم الألكترونى</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-subheader>معهد إعلام</v-subheader>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-calculator-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الحسابات</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-school</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون الطلاب</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-account-group</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون العاملين</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-book-open-page-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>التعليم الألكترونى</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-subheader>معهد علوم صحية</v-subheader>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-calculator-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الحسابات</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-school</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون الطلاب</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-account-group</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون العاملين</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-book-open-page-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>التعليم الألكترونى</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-subheader>المدرسة</v-subheader>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-calculator-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الحسابات</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-school</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون الطلاب</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-account-group</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>شؤون العاملين</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
        <v-list-group>
          <template v-slot:activator>
            <v-list-item-icon>
              <v-icon>mdi-book-open-page-variant-outline</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>التعليم الألكترونى</v-list-item-title>
            </v-list-item-content>
          </template>
          <v-list-item link to="/products/weights">
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>المصروفات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item link to="/products/" exact>
            <v-list-item-icon>
              <v-icon>mdi-circle-small</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>الايرادات</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: null,
    };
  },
};
</script>

<style>
</style>