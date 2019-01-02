<template lang="pug">
  div.team.row
    div.col-9
      div.team-name.row
        div.col-9.content.team-name foobar racing
        div.col-3.corner-down-right
      div.infos-drivers-container.row
        div.driver-names.col-4
          div.driver Foo bar
          div.driver bar bar
        div.team-info-container.col-8
          div.info.row
              div.col-1.corner-up-left.class-gte
              div.col-5.content.class-gte schrottkarre
              div.col-1.corner-down-right.class-gte
          div.info.row
              div.col-1.corner-up-left.class-gte
              div.col-5.content.class-gte schrottkarre
              div.col-1.corner-down-right.class-gte
      div.images.row
        div.col-4
        img.team-car.col-7(src='~/assets/car.png')
     
    div.col-3
      div.team-number 55
      div.team-class LMP2.5
      div.tyre-vendor
        img(src='~/assets/tyre.png')

</template>

<script>
export default {
  props: {
    team: {
      type: String,
      default: 'Team name'
    }
  }
}
</script>

<style lang="scss">
$color: #005294;

div {
  border: 0px solid white;
}
.content {
  background: $color;
}
.corner-up-right {
  border-style: solid;
  border-color: $color transparent transparent transparent;
  border-width: 25px 25px 0 0;
}
.corner-down-right {
  border-style: solid;
  border-color: transparent transparent $color transparent;
  border-width: 0 25px 25px 0;
}
.corner-up-left {
  border-color: $color transparent transparent transparent;
  border-width: 25px 0 0 25px;
}
.corner-down-left {
  border-color: blue transparent $color transparent;
  border-width: 0 0 25px 25px;
}
.team-number {
  line-height: 100px;
  height: 100px;
  text-align: center;
  background: $color;
  font-size: 50pt;
}
.team-class {
  text-align: center;
  background: $color;
}
.info .content {
  padding-left: 0px;
}
.team {
  margin-bottom: 1em;
  color: white;
}
.driver {
  color: black;
  font-size: 10pt;
}
.team-name {
  text-transform: uppercase;
  font-weight: bold;
}
.tyre-vendor img {
  width: 100%;
  background: white;
}
.images {
  margin-top: 1.5em;
}
</style>
