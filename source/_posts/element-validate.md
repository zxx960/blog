---
title: element在循环中校验表单
date: 2024-07-09 13:29:45
tags:
  - element
---

1 element ui在表单循环中进行校验,重点是动态绑定prop的值

```html
<el-form :model="formData">
  <el-card v-for="(item, index) in formData.addMoneyRuleList">
    <el-form-item :prop="'addMoneyRuleList.' + index + '.rule.startAddMinute'">
      <el-input v-model="item.rule.startAddMinute">
        <template #prepend>订单推送成功</template>
      </el-input>
    </el-form-item>
  </el-card>
</el-form>
```

```javascript
const formData = ref({
  addMoneyRuleList: [
    {
      rule: {
        startAddMinute: "",
        startAddMoney: "",
        addMoneyInterval: "",
        incrementMoney: "",
        cappedMoney: "",
      },
    },
  ],
});
```
