<template>
    <div class="card">
        <div class="card-header">
            <slot name="header">
                <img src="../assets/image.jpg" alt="">
            </slot>
        </div>
        <div class="card-body">
            <h3 class="card-title">
            <slot name="Title">
                A Beautiful Flower
            </slot>
            </h3>
            <p>
                <slot name="body">
                 Flowers are nature’s most beautiful gift, a delicate reminder that even in the simplest things, there is extraordinary beauty. They bloom with grace, spreading joy, love, and warmth wherever they go.
                </slot>
            </p>
        </div>
        <div class="card-footer">
            <slot name="footer">
                <button class="btn"><a href="https://en.wikipedia.org/wiki/Flower">Go Somewhere</a></button>
            </slot>
        </div>

    </div>
</template>
<script>
export default{
    name:"Card-C"
}
</script>

<style>
.card {
  margin-left: 40%;
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  max-width: 300px;
  box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
}
.card-header img {
 
  width: 100%;
  height: auto;
}
.card-body {
 -ms-flex-item-align: start;
 padding:10px 20px;
 font-size: 14px;

}
.card-title {
  margin: 0;
  font-size: 18px;
  font-weight: bold;
}
.card-footer {
  padding-bottom: 20px;
  padding-left: 20px;
}
.btn {
  background-color: #007bff;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
a{
    text-decoration: none;
    color: white;
}
</style>