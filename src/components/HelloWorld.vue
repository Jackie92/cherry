<template>
  <div>
    <p>
      <img src="../assets/1.png" alt="" class="panel">
    </p>
    <p>
      <img src="../assets/2.png" alt="" class="panel">
    </p>
    <p>
      <img src="../assets/3.png" alt="" class="panel">
    </p>
    <p class="input-body">
      <img src="../assets/4.png" alt="" class="panel">
      <span class="input-block">

        <span class="list">
          <span class="list-inner">
            <span class="list-name">*姓名</span>
            <span class="list-input">
              <input v-model="name" type="text">
            </span>
          </span>
          <span class="list-inner">
            <span class="list-name">*省份</span>
            <span class="list-input">
              <span class="list-select-modal">
                <select v-model="province">
                  <option value ="volvo">Volvo</option>
                  <option value ="saab">Saab</option>
                  <option value="opel">Opel</option>
                  <option value="audi">Audi</option>
                </select>
              </span>
              <span class="triangle"></span>

            </span>
          </span>
        </span>

        <span class="list">
          <span class="list-inner">
            <span class="list-name">*手机</span>
            <span class="list-input">
              <input v-model="phone" type="number">
            </span>
          </span>
          <span class="list-inner">
            <span class="list-name">*城市</span>
            <span class="list-input">
              <span class="list-select-modal">
                <select v-model="city">
                  <option value ="volvo">Volvo</option>
                  <option value ="saab">Saab</option>
                  <option value="opel">Opel</option>
                  <option value="audi">Audi</option>
                </select>
              </span>
              <span class="triangle"></span>
            </span>
          </span>
        </span>

        <span class="list">
          <span class="list-inner">
            <span class="list-name list-name-long">*经销商</span>
            <span class="list-input">
              <span class="list-select-modal">
                <select v-model="dealer">
                  <option value ="volvo">Volvo</option>
                  <option value ="saab">Saab</option>
                  <option value="opel">Opel</option>
                  <option value="audi">Audi</option>
                </select>
              </span>
              <span class="triangle"></span>
            </span>
          </span>
          <span class="list-inner">
            <span class="list-name list-name-long">*意向车型</span>
            <span class="list-input">
              <span class="list-select-modal">
                <select v-model="cartype">
                  <option value ="volvo">Volvo</option>
                  <option value ="saab">Saab</option>
                  <option value="opel">Opel</option>
                  <option value="audi">Audi</option>
                </select>
              </span>
              <span class="triangle"></span>
            </span>
          </span>
        </span>

      </span>
    </p>
    <p class="submit-block">
      <img src="../assets/5.png" alt="" class="panel">
      <span @click="submitData" class="submit"></span>
    </p>
    <p>
      <a  href="http://www.chery.cn/m/vehicles/tiggo5x">
        <img src="../assets/6.png" alt="" class="panel">
      </a>
    </p>
    <p>
      <a  href="http://www.chery.cn/m/vehicles/tiggo7Year2018">
        <img src="../assets/7.png" alt="" class="panel">
      </a>
    </p>
    <p>
      <a  href="http://www.chery.cn/m/vehicles/tiggo3x">
        <img src="../assets/8.png" alt="" class="panel">
      </a>
    </p>
    <p>
      <a  href="http://www.chery.cn/m/vehicles/tiggo3">
        <img src="../assets/9.png" alt="" class="panel">
      </a>
    </p>
    <p>
      <a  href="http://www.chery.cn/m/vehicles/arrizo5">
        <img src="../assets/10.png" alt="" class="panel">
      </a>
    </p>
    <p>
      <a  href="http://www.chery.cn/m/vehicles/arrizo7">
        <img src="../assets/11.png" alt="" class="panel">
      </a>
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      name: '',
      phone: '',
      province: '',
      city: '',
      dealer: '',
      cartype: ''
    }
  },
  methods: {
    submitData () {
      alert(1)
    }
  },
  mounted () {

  }
}
</script>

<style>
  body,html,p {
    margin: 0;
  }
  h1, h2 {
    font-weight: normal;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  .panel {
    width: 100%;
    display: block;
  }
  .submit-block {
    position: relative;
  }
  .submit {
    position: absolute;
    width: 100px;
    height: 30px;
    top: 10px;
    left: 50%;
    margin-left: -50px;
  }
  .input-body {
    position: relative;
  }
  .input-block {
    position: absolute;
    top: 0;
    width: 100%;
    padding: 48px 0 0 0;
  }
  .list {
    display: block;
    margin: .05rem .45rem 0;
    display: flex;
    display: -webkit-flex;
    display: -moz-flex;
    display: -o-flex;
    display: -ms-flex;
  }
  .list-inner {
    flex: 1;
    display: flex;
    display: -webkit-flex;
    display: -moz-flex;
    display: -o-flex;
    display: -ms-flex;
    height: .22rem;
  }
  .list-name {
    flex: 2;
  }
  .list-name-long {
    flex: 4;
  }
  .list-input {
    flex: 5;
    border: black solid 1px;
    position: relative;
  }
  .list-input input{
    background: transparent;
    border: none;
    width: 91%;
  }
  .list-input select {
    background: transparent;
    border: none;
    width: 123%;
  }
  .list-select-modal {
    width: 81%;
    overflow: hidden;
    display: inline-block;
  }
  .triangle{
    width:0;
    height:0;
    border-width:5px;
    border-style:solid dashed dashed dashed;
    border-color:#e66161 transparent transparent transparent;
    position: absolute;
    right: 2px;
    top: 7px;
  }
</style>
