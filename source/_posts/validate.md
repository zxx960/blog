---
title: element自定义校验规则
date: 2024-07-22 12:29:45
categories:
  - element
tags:
  - element
---

#### 常用的校验方法

```javascript
//校验邮箱，不需要校验空值
function validateEmail(rule, value, callback) {
  if (value === "") {
    callback();
  } else {
    if (!/^([a-zA-Z0-9_-])+@([a-zA-Z0-9_-])+(.[a-zA-Z0-9_-])+/i.test(value)) {
      callback(new Error("请输入正确的邮箱格式"));
    } else {
      callback();
    }
  }
}
//校验手机号，不需要校验空值
function validatePhone(rule, value, callback) {
  if (value === "") {
    callback();
  } else {
    if (!/^1[34578]\d{9}$/.test(value)) {
      callback(new Error("请输入正确的手机号格式"));
    } else {
      callback();
    }
  }
}
//校验数字，不需要校验空值
function validateNumber(rule, value, callback) {
  if (value === "") {
    callback();
  } else {
    if (!/^[0-9]*$/.test(value)) {
      callback(new Error("请输入数字"));
    } else {
      callback();
    }
  }
}
//校验正整数，不需要校验空值
function validatePositiveNumber(rule, value, callback) {
  if (value === "") {
    callback();
  } else {
    if (!/^[1-9]\d*$/.test(value)) {
      callback(new Error("请输入正整数"));
    } else {
      callback();
    }
  }
}
//校验正数，最多两位小数，不需要校验空值
function validatePositiveFloat(rule, value, callback) {
  if (value === "") {
    callback();
  } else {
    if (!/^\d+(\.\d{1,2})?$/.test(value)) {
      callback(new Error("请输入正数，最多两位小数"));
    } else {
      callback();
    }
  }
}
```

#### 使用方法

```javascript
<el-form-item
  label="age"
  prop="age"
  :rules="[
    { required: true, message: 'age is required' },
    { validator: validateEmail, trigger: 'change' },
  ]"
>
</el-form-item>

```

#### 提交前校验

```javascript
function submitForm(formEl) {
  if (!formEl) return;
  formEl.validate((valid) => {
    if (valid) {
      console.log("submit!");
    } else {
      console.log("error submit!");
    }
  });
}
```
