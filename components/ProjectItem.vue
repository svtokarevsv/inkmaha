<template>
  <div>
    <div class='project-item' :class='getColSpanClass(item.width)'
         v-bind:style="{ 'background-image': `url(${item.url}` }" @click='showPopup=true'>
      <p class='text-gray-50 project_name'>Some name</p>
    </div>
    <div v-if='showPopup' class='overlay flex justify-center' :class='showPopup?"show":""' @click='clickOutside'>
      <div class='wrapper items-center mx-4 max-w-full w-full h-full lg:max-w-screen-lg isolate light-modex relative height-fit'>
        <div class='snakable border-gray-50 text-gray-50 hover:border-white hover:text-white top-right' @click='showPopup=false'>
          <div class='close-icon'></div>
        </div>
        <main class='mt-0 pt-0 popup'>
          <h2 class='max-w-5xl mb-5 text-gray-50'>{{ group.name }}</h2>
          <div class='popup__content' ref='popup_content'>
            <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam animi architecto
              distinctio dolor ducimus, iure similique veniam veritatis voluptas? Accusamus animi
              facilis fugit libero modi nemo odio quasi quia recusandae!
            </div>
            <div>Accusantium ad alias aspernatur consequatur consequuntur cum deserunt dignissimos
              dolores dolorum, error esse est ex obcaecati optio perferendis possimus rem
              repellendus tenetur, vero voluptas. Incidunt iusto magni odio ratione ut?
            </div>
            <div>Accusamus accusantium adipisci blanditiis, deserunt distinctio et eum
              exercitationem illo magnam minus, necessitatibus neque nesciunt nulla officia
              provident ratione repellat voluptatibus! Autem fugiat illo laudantium nemo officiis
              quidem rerum voluptatem.
            </div>
            <div>Dolores, quidem, voluptas. Deleniti doloremque necessitatibus odit! Accusamus alias
              architecto cumque ducimus labore, modi sint tempora. Consequuntur distinctio iure
              necessitatibus praesentium quibusdam quis rem, ullam vero! Consequuntur laborum
              perferendis rerum.
            </div>
            <div>A animi assumenda aut cum deleniti dicta doloremque eaque et eum itaque iusto
              labore magni, mollitia necessitatibus nesciunt nisi odio omnis provident quisquam
              sequi similique sit tempore ullam veritatis voluptate.
            </div>
            <div>Aspernatur consectetur, deleniti dicta distinctio dolorum eligendi facilis fugiat
              id inventore, laborum libero placeat quis quod reprehenderit repudiandae unde ut. Amet
              deleniti dolorem ipsam labore minus molestias nesciunt repudiandae tempore!
            </div>
            <div>Aspernatur assumenda culpa doloribus et eum exercitationem fugiat fugit impedit
              nemo, neque odio quis repellat reprehenderit similique vel? Accusantium aliquid,
              dignissimos eius fugiat id nisi porro quisquam! Quis, sit soluta!
            </div>
            <div>Ad assumenda, cumque iste maiores odio velit! At cum enim ex facere magni mollitia
              nisi nobis, nostrum omnis praesentium quod sint sit veritatis. Deleniti praesentium
              quaerat quo veritatis voluptate voluptatibus?
            </div>
            <div>Asperiores blanditiis debitis dicta ea exercitationem maxime mollitia, non nostrum
              placeat reprehenderit sunt tenetur ullam vero! Alias architecto, ducimus itaque nobis
              quisquam quos tempora. Autem dignissimos ipsam itaque molestiae numquam?
            </div>
            <div>Assumenda ipsa ipsam iste pariatur perferendis possimus temporibus veritatis. Autem
              consequuntur corporis debitis dignissimos dolores ea esse illum iste, magnam minima
              non quae quas quia quisquam ratione soluta, unde vel.
            </div>
            <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet asperiores autem
              corporis eos ipsam laboriosam laborum minima minus natus nobis optio quae quas quia
              recusandae repudiandae, sequi sit tempore vel!
            </div>
            <div>Aperiam eligendi perferendis quaerat qui tempora. Consequuntur cupiditate fuga,
              incidunt iure libero molestias quam saepe unde voluptates voluptatibus? Error
              excepturi id illo illum laboriosam maxime mollitia porro unde veniam veritatis.
            </div>
            <div>Adipisci esse et facilis fuga iure magnam, neque quibusdam quis quod, saepe soluta
              unde? Commodi debitis eaque id ipsam modi neque tempore! Consectetur fugit quasi
              repellendus suscipit vero. Maiores, non.
            </div>
            <div>Aliquam, aperiam architecto assumenda consectetur consequatur debitis dolorum,
              expedita itaque iure neque possimus quasi qui sapiente, soluta velit vitae voluptatum.
              Autem beatae blanditiis eveniet iusto perspiciatis rem reprehenderit sunt suscipit.
            </div>
            <div>Consequatur dolor ducimus ipsam, laudantium perspiciatis rerum saepe? A assumenda
              commodi dicta dolor doloribus eos error est et harum nisi nostrum officiis perferendis
              possimus quibusdam quidem, quis quos temporibus voluptatum?
            </div>
            <div>A, amet atque autem et eveniet expedita, facere, magnam minima nam officia
              perferendis quis reiciendis unde! Alias animi autem consectetur doloremque eligendi
              excepturi, facere magni molestias neque quae, saepe veritatis.
            </div>
            <div>Accusantium at consectetur debitis deleniti dicta dolorem eius expedita illo
              laboriosam, minima minus odio odit, perferendis quibusdam repellendus repudiandae sunt
              voluptates. Animi culpa ducimus eveniet explicabo fugiat inventore, neque
              voluptatibus?
            </div>
            <div>A asperiores, atque, blanditiis commodi cum dicta, dolore ducimus fuga harum in
              ipsum magni minima nesciunt perferendis quaerat quam quod reiciendis repellat sequi
              sunt veritatis vero voluptatibus voluptatum! Consectetur, omnis?
            </div>
            <div>Aliquam at blanditiis dicta est facere labore maxime quam sequi voluptate
              voluptates. Ab autem eaque est facere, in incidunt ipsum maxime minima nam quasi
              quibusdam quidem quisquam reiciendis, rerum ut?
            </div>
            <div>Debitis deserunt eos nostrum quod quos recusandae! A, adipisci asperiores at aut
              culpa delectus deleniti dolor eveniet incidunt ipsa ipsum iste magni, obcaecati porro,
              praesentium quibusdam repellat totam ut voluptatibus?
            </div>
            <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid consequatur
              dolorum eius eveniet hic in iste iusto labore magnam nam odit possimus provident qui
              quia quo sapiente, ut veritatis voluptates.
            </div>
            <div>Asperiores, at consectetur debitis ducimus impedit nobis non numquam reprehenderit
              similique! Accusantium adipisci asperiores aspernatur aut autem blanditiis, cum,
              doloribus excepturi facilis laborum natus placeat quos, rem tempora temporibus!
              Consequatur!
            </div>
            <div>Aspernatur consequuntur cum enim facilis laudantium pariatur vitae. Amet architecto
              atque corporis, delectus dolorum ea error, esse id illum ipsum numquam odit
              perspiciatis porro quae ratione reiciendis sequi suscipit vel.
            </div>
            <div>Ab at corporis cum debitis doloribus enim fugit, illum in laborum neque obcaecati
              quis quod recusandae repudiandae saepe. Cum excepturi necessitatibus numquam officiis
              perspiciatis quaerat quidem rerum sapiente sint suscipit.
            </div>
            <div>Ab aperiam assumenda at corporis delectus dignissimos dolor dolores ex fuga fugiat
              fugit, iure labore, molestias necessitatibus obcaecati officiis omnis qui quibusdam
              quo ratione reprehenderit repudiandae tempore temporibus ullam vel?
            </div>
            <div>Aliquid animi consequuntur delectus dolores eos expedita facilis fuga id iusto
              libero minima minus neque nobis non nulla officia, omnis quas quibusdam quis
              recusandae repellat rerum saepe, vero. Cum, incidunt!
            </div>
            <div>Amet culpa eius enim esse eum, ex exercitationem harum impedit in ipsam ipsum iste
              laudantium maxime molestias nam non omnis optio quam quia quos reiciendis rem, sed
              voluptatem voluptates voluptatum?
            </div>
            <div>Ab alias aliquam corporis doloremque eos harum minima natus, odit pariatur
              praesentium, quasi qui quidem quisquam ut velit! A adipisci debitis deleniti excepturi
              itaque neque nesciunt pariatur quibusdam quidem unde.
            </div>
            <div>Accusantium, cumque dolore est facilis inventore iusto, obcaecati omnis perferendis
              quae repellendus repudiandae sunt suscipit, veritatis voluptatem voluptatibus? Ab
              deleniti dignissimos expedita ipsa, laborum minima molestias nobis quis suscipit
              ullam?
            </div>
            <div>Aperiam corporis distinctio eum excepturi facere harum hic labore laboriosam
              laudantium libero magnam maxime minima numquam placeat quaerat quis quos similique
              sint, tempora vel! Alias eaque eos odio repellat! Placeat!
            </div>
          </div>
        </main>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectItem',
  props: {
    item: Object,
    group: Object,
  },
  data: () => ({
    showPopup: false,
  }),
  computed: {
  },
  methods: {
    getColSpanClass(width = 1) {
      switch (width){
        case 1:
          return 'col-span-1'
        case 2:
          return 'col-span-1 md:col-span-2'
        case 3:
          return 'col-span-1 md:col-span-2 lg:col-span-3'
        case 4:
          return 'col-span-4 md:col-span-2 lg:col-span-3'
        default:
          break
      }
    },
    clickOutside(event) {
      if(this.$refs.popup_content === event.target || this.$refs?.popup_content?.contains(event.target)) return;
      this.showPopup = false
    }
  }
}
</script>

<style scoped>

</style>
