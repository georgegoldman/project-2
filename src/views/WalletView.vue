<template>
  <div class="row mt-5 py-5">
    <div class="col-12">
      <div class="d-flex justify-content-center">
        <h3>Wallets</h3>
      </div>
      <div class="d-flex justify-content-center">
        <p>
          Multiple iOS and Android wallets support this protocol. Your private
          keys are encrypted locally on your device with Secure Enclave,
          protected by Biometric and 2-Factor Authentication.
        </p>
      </div>
    </div>
    <div class="col-lg-3 col-12" v-for="wallet in wallets" :key="wallet.name">
      <v-card class="mx-auto">
        <v-img class="white--text align-end" :src="wallet.image"> </v-img>

        <v-card-actions>
          <v-btn color="dark" text> {{ wallet.name }} </v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "WalletView",
  data() {
    return {
      wallets: [
        {
          image:
            "https://miro.medium.com/max/400/1*fcTciSnhZO3S7QwGkQWJDA.jpeg",
          name: "waveduck",
        },
        {
          image: "https://www.fintechfutures.com/files/2018/01/Ledger-logo.jpg",
          name: "ledger nano",
        },
        {
          image:
            "https://www.clearos.app/assets/uploads/apps/com.wallet.crypto.trustapp/latest/logo.png",
          name: "trust",
        },
        {
          image:
            "https://cdn.iconscout.com/icon/free/png-256/metamask-2728406-2261817.png",
          name: "metamask",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/nJQ2XyuF3tWPspfAMy4kVEk5YLg2n-ZJQ_qExNagaPYiIfV_D3PW3_iAPBq8DY_uLw",
          name: "tronlink ",
        },
        {
          image: "https://onlinehackz.com/api/icon/5c9c56cce8eac41a20f18283",
          name: "Atomic ",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/P-xt-cfYUtwVQ3YsNb5yd5_6MzCHmcKAbRkt-up8Ga44x_OCGLy4WFxsGhxfJaSLEw",
          name: "argent",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/sOEtBfKNBojqQkiU8_3uhV8jtxbJgBmbh1kQbG9mE-gdL-U5QC_B6CZBM3tTp5G6jQ",
          name: "coinomi",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/Ja-xk6ZTXzuGVvqfTRJahBBwJLFE-Dz8pEdyjfRM9jz87fDA_hdYDe3QM70EzyquDw=w240-h480-rw",
          name: "imtoken",
        },
        {
          image:
            "https://nexaglobal.io/assets/main_website_assets/img/auth/tokenPocket.png",
          name: "tokenpocket",
        },
        {
          image:
            "http://medishares.oss-cn-hongkong.aliyuncs.com/logo/math/MathWallet_App_Icon.png",
          name: "mathwallet",
        },
        {
          image:
            "https://lh3.googleusercontent.com/mMR-DMxtaE0VKnrcaNx1lCm7OxnZZzjdUjX_D33fPB0GRHHZ7s3O-YynK77e4qXBsZQ",
          name: "pillar",
        },
        {
          image:
            "https://defirate.com/wp-content/uploads/2020/02/TOIXMgdS_400x400-300x300.png",
          name: "autherem",
        },
        {
          image:
            "https://is2-ssl.mzstatic.com/image/thumb/Purple126/v4/a0/c5/e3/a0c5e3e5-a5c0-38d8-196f-55985402f43b/source/512x512bb.jpg",
          name: "rainbow",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/23jazn0vCwSUoRu0SkVtMrcRbah372j6xIhsP1fUIpImq3ReRKvOXKNDnEOWe-CqDTvO",
          name: "eidoo",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/JujGZjn2HIFYuToiXn9ZMDfH59BwcZoEvasayCSpp6R6JFaIyeaJu4tcqTiCakBPYHg",
          name: "Zelcore",
        },
        {
          image:
            "https://static-s.aa-cdn.net/img/gp/20600013434661/8aXTeaP1Sm29QPQ1IWacpgBRMpyCQLlVtA5QQ0DhN30d-R0fCdrCHlbQUZvdg2bJGvQ=s300?v=1",
          name: "Defi",
        },
        {
          image:
            "https://aws1.discourse-cdn.com/standard20/uploads/gnosis_safe/original/1X/175f55ca5dfa29e9322ebc0d8aa73f11e6fde6db.png",
          name: "gnosis safe",
        },
        {
          image:
            "https://pbs.twimg.com/profile_images/1343592183451037702/ng1uSrX2_400x400.jpg",
          name: "gridplue",
        },
        {
          image:
            "https://res.cloudinary.com/crunchbase-production/image/upload/c_lpad,h_256,w_256,f_auto,q_auto:eco,dpr_1/evj35bp9fcnm1ouqvmsu",
          name: "cool wallet s",
        },
        {
          image:
            "https://www.yadawallets.com/wp-content/uploads/2021/01/Alice-wallet-logo.png",
          name: "Alice",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/TkIzwGw3athIXQX9BArx2Ejn9u77_GW0So1DnuYGeWHyTu42cnHt1yPCoi3iZKuUfQ",
          name: "Alpha",
        },
        {
          image:
            "https://is4-ssl.mzstatic.com/image/thumb/Purple126/v4/70/b6/c5/70b6c542-7dac-4e79-c9ad-a76599c94de6/source/256x256bb.jpg",
          name: "Tokenary",
        },
        {
          image:
            "data:image/jpeg;base64,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",
          name: "safe pal",
        },
        {
          image:
            "https://www.yadawallets.com/wp-content/uploads/2021/01/Equal-wallet-logo.png",
          name: "Equal",
        },
        {
          image:
            "https://cdn6.aptoide.com/imgs/2/a/5/2a5a9029eca64b05cd4927a5c2ede986_icon.png",
          name: "infinito",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/7aPjIqSxe5mNlbHdlxhXNRd3FxqoX4zR8EdwQr0XR3uxWyWiUSMTTwx1VlE36OZAksk",
          name: "walleth",
        },
        {
          image:
            "https://www.yadawallets.com/wp-content/uploads/2021/01/MyKey-wallet-logo.jpg",
          name: "mykey",
        },
        {
          image:
            "https://is5-ssl.mzstatic.com/image/thumb/Purple115/v4/1b/92/db/1b92db36-eda3-fed2-13aa-cd65f6f9cdc3/AppIcon-0-0-1x_U007emarketing-0-0-0-10-0-0-sRGB-0-0-0-GLES2_U002c0-512MB-85-220-0-0.png/1024x1024bb.png",
          name: "spatium",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/WDgpN0B2MlEMJQFzLG1dxrjkgB2lMLhxCQlVC-subnPcUCf9s_tn7TpmpsabuVNNo3Q",
          name: "wallet.io",
        },
        {
          image:
            "https://images.g2crowd.com/uploads/product/image/large_detail/large_detail_4166fd82728b86aba74e45b1a77b6c09/infinity-wallet.png",
          name: "infinity wallet",
        },
        {
          image:
            "https://www.yadawallets.com/wp-content/uploads/2020/10/ownbit-wallet-logo.png",
          name: "ownbit",
        },
        {
          image:
            "https://www.yadawallets.com/wp-content/uploads/2021/01/Easypocket-wallet-logo.jpg",
          name: "easypocket",
        },
        {
          image:
            "https://cdn6.aptoide.com/imgs/2/5/3/253661d41f9dae4106ae1b2fce9e3925_icon.png",
          name: "onto",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/MPhruuIOGD4_var3n8ikpy8yixsPLq8g4zoneqBPA0XZNlVzUc1iK2S-8YN59znhrxYu",
          name: "bridge",
        },
        {
          image: "https://sparkpoint.io/images/sparkpoint-logo-top-one.png",
          name: "sparkpoint",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/HusrjtJaiFk2nj6FfYQbewVKIHkmO9KwivN-X-_pOdk0wHrLneT7JfKtXHr7XWCJ0A",
          name: "via wallet",
        },
        {
          image:
            "https://walletscrutiny.com/images/wallet_icons/iphone/io.nash.app.jpg",
          name: "nash",
        },
        {
          image:
            "data:image/png;base64,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",
          name: "bitkeep",
        },
        {
          image:
            "https://walletscrutiny.com/images/wallet_icons/iphone/com.visionsoftware.vision.jpg",
          name: "vision",
        },
        {
          image:
            "https://is1-ssl.mzstatic.com/image/thumb/Purple125/v4/a2/77/98/a27798f0-b31c-d891-98cc-fad65b6df30d/source/512x512bb.jpg",
          name: "swift",
        },
        {
          image: "https://peakdefi.com/assets/img/logo.png",
          name: "peak defi",
        },
        {
          image: "https://synchconnects.com/wallet/xdc.png",
          name: "xdc wallet",
        },
        {
          image:
            "https://is1-ssl.mzstatic.com/image/thumb/Purple126/v4/4c/40/52/4c405240-ebd4-b6e0-c4e0-d5cfdcdf0b76/source/512x512bb.jpg",
          name: "unstoppable",
        },
        {
          image: "https://cryptologos.cc/logos/meetone-meetone-logo.png",
          name: "meet.one",
        },
        {
          image:
            "https://s2.coinmarketcap.com/static/img/coins/200x200/2675.png",
          name: "dock wallet",
        },
        {
          image: "https://synchconnects.com/wallet/at.png",
          name: "AT.wallet",
        },
        {
          image:
            "https://s2.coinmarketcap.com/static/img/coins/64x64/10903.png",
          name: "coin98",
        },
        {
          image:
            "https://is3-ssl.mzstatic.com/image/thumb/Purple126/v4/0c/68/7f/0c687fa3-cd11-d8a4-f03b-4a3441abac68/source/256x256bb.jpg",
          name: "morix wallet",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/JRgNmT2Z7BlV2cKxfclRYjOQHOJNnPCoGW4UvIxmH_tX9HSvg4WAnn10uCkZQEUrqiU",
          name: "midas wallet",
        },
        {
          image: "https://synchconnects.com/wallet/vault.jfif",
          name: "Trust vault",
        },
        {
          image:
            "https://www.yadawallets.com/wp-content/uploads/2021/06/Phantom-wallet-logo.png",
          name: "phantom",
        },
        {
          image:
            "https://pbs.twimg.com/profile_images/1414558597854474242/ceAKhnLD_400x400.jpg",
          name: "aktionariat",
        },
        {
          image: "https://avatars.githubusercontent.com/u/39907240?v=4",
          name: "aktionariat",
        },
        {
          image:
            "https://is3-ssl.mzstatic.com/image/thumb/Purple126/v4/53/05/1e/53051e82-358b-4d5e-f7b4-e6b84c367a9a/source/512x512bb.jpg",
          name: "keyring pro",
        },
        {
          image:
            "https://www.yadawallets.com/wp-content/uploads/2021/02/CYBAVO-wallet-logo.png",
          name: "cybavo",
        },
        {
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRCNjsjbnC9zV2D97JPFvboglXba_Xq4TImkg&usqp=CAU",
          name: "loopring wallet",
        },
        {
          image:
            "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAAAclBMVEX///8dICgMERx7fIAZHCUsLzfExMUAAAze3+A0Nj0AAADk5OUSFh8XGyMpLDTKysv19fXq6+vW1tdhYmZzdXmur7FBQ0oAAAanqKqGh4sAABMECxcOEh2QkZUgIywVGiVZW1+dn6KPkJNoam63uLo5PEM14Rt4AAADdElEQVR4nO2d25KaQBBAGRYFWfCCiLqjeIv//4txN6msqR1nKizdauWcZ7XnVENDDdgdRQAAAAAAAAAAAAAAAAAAAAAA0AezajK8xvWZavh9JtVMW+2dbDtv2jj9JN+5Plbn6beJ22a+zXT1potmaYvSXFMOXJ98iU0PlIVdNoupnt9qZMsvq0gEDT8s7Wil5Jjt08SxAmnDS4R0r3KsrvLCHV/c0JgiX8kLrm8tWcPQmHgtLVi/3YotWWmueKtlBdc3BZVyeFEUzeLKs14tQxMLnotZ7gmsZmhysYo63burqLZhsZe6Lq5SX1ylSvNOKnScTkeuC/0f9HJokpFMEhfWH1bP0NiFiGHz9V70XoZlIyGYLf1RNQ3NUqKcbv0HqWaluRymWwHDue9SYZRzWMz7F5wFTkNdw7Lpf2OjagNBVQ1NW/VuOAktVdcwnvRuOPTe0BjlSmNS586erKFuDjHEEEMXVBoMMcRQ3vD5K02e+CnGz264G/gZO3cWnsiwIxhiiOH9wRBDDO8PhhhieH8wxBDD+4Mhhhj2yGz9EqB2PVp/IsNsbGM/+euTG/rfaruAIYYYYoghhhhiiCGGGGKIIYYYYoghhhhiiCGGGGKIIYYY/jbs9vywTgPf6kj+MM+AF3Xoa92o+/+nMwAAAAAAAAAAPAavzbhLX4x1G2in0TpbO4eCDXYS+6VFp94mNtASxb64vjYOBEsEdhODO8Id+9PETsNBoA3lXfa8O/YYumEY2mDHEEMMXVBp/s3wEXOIIYb3NzwHTv6nrzRS/bw75lCgF3TkHd+hbijQzzuqNw9kKNGTPToEJgeoGkr01feP0THKlUZkNsI0UExVcygy3yI6ikxh6WRYiMwoiTL/dARNw1hmzkx08q5W0bA8Cw18qnbesHqVJhVK4eWCcXuunGYONye5WZat575GzTBxvgTZE5nn6NEyTErR9kJDezO0luHbQVIwin44psj+QqfSJNKClywObpyLKjksjcKo1ax1V1QNQ2t1Xg0+7FzLljfcbI5aY52rU/v1dBQ2LK2Za77bnR3Pud0UZfntyQFuw+una2VZbGx+Pmq/uz7NDvW+OY8+cd7vB2er5875vs3V756bfX3I9MaO/8Usu8J5p1H5Bt9/4EzN6/UPC2xYAAAAAAAAAAAAAAAAAAAAAAD8p/wEUAVlt99kiIwAAAAASUVORK5CYII=",
          name: "Ledger live",
        },
        {
          image:
            "https://play-lh.googleusercontent.com/DfD8BH0veJ1lCAdlZBfVj5HdK6-vjl9UcFxLGIuyc2RvQs-KCiW4yJKWz-4gSkNy5RA",
          name: "maiar",
        },
        {
          image: "https://bitpay.com/favicon.ico",
          name: "bit pay",
        },
        {
          image:
            "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAoHCBYSFRgSFRQZGRgSHBgYEhgZHBoZGRoWGhgdHBoeGRYcIC4nHB4sHxgYJjsmKy8xNTU1HCQ7QDs0Qy80NTEBDAwMEA8QGBISGDEdGB0xNDQxNDQxNDE0NDQ0NjQ0NDExMTE0MTQxPzExPzE/NDExPzQ0PzQ0Pz80PzQxMTE/Mf/AABEIAOEA4QMBIgACEQEDEQH/xAAcAAEAAgMBAQEAAAAAAAAAAAAABgcDBAUIAgH/xABEEAACAQMBBQUGBQIDBAsBAAABAgADBBEhBQYSMUEHIlFhcRMjMkJSgRRicoKRFaGSscEkVGOiFyU0NUNzsrO00dMW/8QAFgEBAQEAAAAAAAAAAAAAAAAAAAEC/8QAGREBAQEBAQEAAAAAAAAAAAAAAAERMSFR/9oADAMBAAIRAxEAPwC5YiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiJw9ob2WNuStW7pKw5rxBmHqq5I5dYHcic272xQo0hcVKqpTYKVdzw8QYZXCnUkg8sZ8pA9rdrdJSVtrd6ng9Q+zQ+YXBYj1CwLOiUTc9qV+5PCaNMa4CoSR93Y5P2+00E7Q9pggm7Jx0NKhg+uKYP95cTXoWJR1n2rXqHvpRqL4cLI32YNgf4Tzkv2N2qWtYha6vQY/Me/Tz+tRkepUDzkNWFEwWt0lVQ9N1dWGVZCGUjyYaGZ4UiIgIiICIiAiIgIiICIiAiIgIiICIiAkG3u7Q6FkWo0wK1ddGUHCUz/AMRx8w+ka+PDmRztD7QCS1nZvgDK166nUnkUpt083HoPGV3sXZNS7rJbUVy7n9qKPidiOSj/AOhzIErNruvtXaO2q3sFdm4sk00Jp0VTkS+Oa+bFjk4HQSVVNmWW79JatRRcXjD3KtoqkaFlXXgQfUcsc4GOQk9KjbbAsmf4iMcTcnr1iO6vXA54GoVQT4k0htjalS7rNcVm4mc/ZV+VEHRQDoPU8yTBx9bZ2xWvKhrXDlmOeHoqKT8KJyVeXrjUk6zQidrYG611fa0KJKdaj9ymP3kd4+IUEiUcWJa1h2QaZr3Z/TSUDHL53Jz1+UdJ0/8Aohs/94uv8VH/APGTTFLRLavuyBMe4u3B6Cqiv/zJw4664MhG39yryyyz0uNBn3lLLoB4uMcSDzIA84MaOwdv3Fi/tLeoVBOWQ603/WnIn8wwR0Mu3c3fSjtFeD4K6jNSkTnQaFkb5l19RnXoT59Bma0uXpOtSm5R0IZGXQqw6j/LHIgkHQwSvVESK7ib1LtKhlsLXpYWug0GTydRz4WwfQgjpkyqRoiIgIiICIiAiIgIiICIiAiIgJWvajvgbdTZW7kVagzWdTg00PJQejMOo1A15kGSrfLeJdn2zVjgu3coKT8VQjTPkBlj5Cedriu9RmqOxZ3Ys7HmzMckmVLWNEJIVVJJIVVUZJJOAqqOZJwABL+3C3VXZtAs+Pb1QGrt0UAZFNT9K65PU5PgBD+yTdfjb+o1V7qkrag8i3J6n21UefEegM7Ha3vL7GkLKmfeXKk1cfLQ5EH9Zyvor+UJPqAb/bznaNwSjH2FHK0B0b6qhHi2NPBQOWTIuTiJZHZhuZ7dlvrhfdoc26MNKjD5yD8oPLxIzyGo6y7gdngrBbq9Q8J1pUDpxLjRqo5hTzCdeumkt1KYUBVAAAAAAwAB0AHITJEjSAby7K2y5Y297T4CThEUUWCnkAxDEnz4xK52ptba1owW4rXNM57vExKk8+64yj/YmehZgurVKqGnURXVhhlcBlI81OhlTFIbI7T76iQKpW4XPeDqEfH5XQAD7q0tTdbey32ipNJirqM1KT4FRfPHJh5jI9OUr/ffs1NFWuLIMyDLVKGSzKOZNMnVh+U5PhnlK5s7p6TpVpOUdCGR1OoPl4jyOhGhyITcXLvp2dU7oNXtQtOvgkqNKdU89RyVvzDQ518RTFei1NmpupR0JV1YYZWHMEeM9C7j7yrtG3FQ4FWnhLhRoA+PiUfSw1H3HQyK9rm7IdP6hTHfp4W4A+annCsR4qSBn6Tr8IgsVvurt1rC5S4XPCp4ayj56TfGMdSNGHmonpOlVDKHU5VgCpHIgjII+08qy+OyjaZr2Coxy1szUT+kYZB6BGVf2xSJtERI0REQEREBERAREQEREBPh2ABJOANSTyA859yue1zeP2NAWSN7y6B9rg6rQzggj85BX0DQK7363jO0blqin3NLKW4/LnvN6sRn0CjpNHdfYb39ylsuQG71Vh8lJSONvXUKPNhOSTjWXz2Z7t/g7YVHXFa5CvUzzVOaJ5YByR4k+ErM9SOq9Gxty2AlG2TkPlRF0AHU6Yx1JnnHbW1Hu673NT4qrZ4c5CLyVQfBVAHnjPWWR2ybf+CwQ88Vbj0B92p+4LftXxlZ7M2e9zVShSXieqwVR0HizeCgZJPgDEK7+4O6p2jX7+RQokNXYacXVUU+LdfBc8iRPQFGkqKqKoCqAqqBgAAYAAHIATm7t7Ep2NulvT1CjLMebOfiZvMn+AAOk68iyEREKREQEpXtT3TW2f8AG0FxSrNiso5JVY5DDwVv7N+rS6pztv7NW7t6tu3/AIqMoPg2O632bB+0FUx2TbRNG/Wlnu3SMjDxZFLqftwuP3GXjdWy1Uak6hlqKyODyKsCCCPQmed9wkLbRtRjB9pkjkRwozNz8AD/ABPR8tSPLN/aNQq1KDfFRd0J8eBiufvjP3lk9iVyeO6pdCtJ15cwXVteeoK/xIp2jUfZ7SugOrI2gxq9JGP9yZI+xT/tFx4eyTP+PT/WEnVyxESNkREIREQEREBERAREQNPaV8lvSevUOEpKzueeijOg6noB1Jnmzbm1XvLipcv8VRsgfSg0RR6KAPPU9ZYfbDvHkrs+m2i4qXOOp5oh/wDWf2ecrG3oNUZaaKWd2VEUcyzHAH8mWM1L+zLdz8Zciq49zakM+Ro1Tmi/z3j5KB80u7al8ltRqV6hwlJS7eOAOQ8SeQHiZo7qbCWwtqduurKOKq311G+NvToPAACQPtk29olgh54q3GPAH3an7gt+1fGF4rLam0Hua1S4qfHWYs3lnkoPgqgKPJRLe7J92PYUvxtQe8uFHsgRqlHmD6tofQL5yvdwd2/6hchWHuaOHuPBhnup+4gj9IbriehlGNB9oqR9RESNEREBERAREQKp7PN32O0Ly7YEJb1rmlRJ+ZzVYMR48KjGfFvKWtPwDEx16qorOxAVQWYnkFAySfsIHn3tJqB9p3JHRqa/daKAyW9iNqeK6rHliki+vfZv7FJWu1L03FarXPOs7vg4BAdiQDjwBA+0vHsu2Wbewpsww1yWrN+l8BP+RUOviZUnUziIkaIiIQiIgIiICIiAnJ3j2yllb1LlteAd1erOdFUepI+2TOtKM7Vd4vxNyLVGzStSQ2OTV+Tn9oyvqWhKhV3dNWd6tRuJ6jF3bxZjk+g8B0GBLN7IN2sk7RqLovElqCOvJ6g/ug/d5SBbsbDe/uEtkyA3equPkprjjb11AHmwnpCztUootKmoVKahUUcgqjAEtSPnaN6lvSes5wlJWdz+VRk4855p2hd1L24eqVLVLl8qg1OWIWmi+g4VHoJZfbJt/CpYIdXxVuP0A9xD6sOL9i+Mwdke6/Ef6jVXReJLQEczyep/mo/cfAwX1PNzd3l2fbLRGC7d+uw+aoQM4/KAAo8gPOSCIkaIiICIiAiIgIiICV72t7wChb/hEPvLsEMPpoA98n9R7vmOLwkr3j25SsaLV6p0XREHxO+O6iDxP9hknQTz/d3FxtO6L8JetcNhEXkqj4VB6Io6nzJ6ypazbm7AbaF0lHB9mveuG6Ckp1GfFvhHqT0M9HIoAAAwBoAOQA5Yke3K3YTZtAUwQ1R8NcP9T45L4KuoA8yeZMkkhIREQpERAREQEREBETU2heJQptWqMFSmCzk9AP8AM9AOpIgRztE3l/AWx4D7+vlKA6rp3nx4KCPuVnn8Dpqf5JP+pM6+9G3Xv7h7h8gHu0l+imCeFfXUknxJ8pMuyndP2ri/rL3KZ/2ZT89QHV8fSp5fm104Rms9TXs73Y/p9vlwPb18PWP0j5Ez+UE58yfKSPal8ltSevUOEpKXfxwByA6k8gPEzdlT9r23jUZNmUsszFXrKupLkj2VMDqSSGx+jxka4h+x9n1dtX7M+R7VjUuWGvs6QwAobx4QqL6Z6GegbagtJFpooVKahEUaAKowAPQCR/cTdobPtxTODVqYa4YfXjRQfpUaDx1PWSeEhE1b68WgjVXzwIOJiFZiAOZ4VBJ+wn7ZXlOugqUnV0b4WUhgfQiFat5ty3o1VoVayI9QcSK54eIZI7rHQnI5Zzy8ROipyMjkeRmC9sqddDTqoro3xK6hlP2MidfcNaeWsLqvaNqQisXoZJyc0XPryOBnl0gTWJAWfblr8tteKOo91UI+5VQevXrPj/8AvrmnpcbIulIxrTDVEOR9XABnyyfWE1YMSvK/arRTRrK7VuiuiJ/OXz/aatftJuX0obKrNkaMwqNrryVKZ4hy14h1g1Zsi+9O+lts9SrN7Stju0UI4vLjPJF8zr4A8pC61Lb+0O6w/DU254IojB9C1Xl0nR2F2UUaZD3VQ1mzkomUp5595s8T651yuc6iDUJKX237guFyE7oOq0aCk5xnq2ME4yzYHQDFubo7o0dnU8J36rD3lVhhm8lHyLp8I++TrOjs65t1ZrSgUBtlXjpUwAtMNnhDcIwpOCeHn1xOpBhERCkREDi7f22LI0nqJ7io3BWrZwKLNgU2ZcfASSC2Rw6c86dhTnUdZhvLVKyNSqKGSoCrqeRUjBBkCobQq7CcW9xx1LBzi2r6u9DPKnUAGWUdOuOWfhULFiYLW4Sqi1Kbq6uMqykMpB6gjnM8BETFVqqil2YKqglmJAAA5kk8hAyEyje0vfD8Y/4Wi3+z0W7zA6Vag66c0Xp4nXopm32g7/8A4kNaWjH2J0rVRkGp4onUJ4n5uXw/FEt192620aop0lwgI9rUI7iL5+LeC8z5DJFZtbm5G6z7Sr8JytGng3DjQ4PJFP1Nj7DJ8M+gra3Wmi00UKiAKiqMKqgYAA6ACa2xdk0rOitvRXhRB92bqzHqxOpM6EiyOZt/ayWVvUuX+GmuQOrMdFUeZYgfeV/2abAe4qNti6GXqlmt8jGS2jVAOi47q+QJ+kzb21SO2r38IrH8FYNm6ZScVK/VAw6gZXTllzz4ZYlOmFAVQAFACgaAADAAHhAyREQpIntLdVqbtc7PrfhqzavTxxW9Y/8AEpfKxxjjXBksiBCLffn2DLQ2nQa1qHRagy9u58UqLnh8cHOBzIkvtbpKqCpTdXVtVZCGUjyYaGLu0Sqhp1EV0bRldQykeanQyG3XZxSRjUsq9a0c5Pu3ZkJP1IWBI8uLHlAnUSvDa7fts8Fe2ulHw8ahHOnLACDn4ufXpPwbwbbXutsumzDmyuoUnyHtDj+YTViRK5bbm3n0TZ1JMcy7K38e+X/Wfg2Btq6JFxtBKCHHdoDvY64KqpGcD5zzPpAl+294rayXiuK6p1C/E7fpRcsfXGJG6W0L7a2lBXs7Q867gfiaq/8ABXkgI+fXmCCcETd2H2e2ds3tWVq9bOTUrnjOfEL8OdBgkFh4yX4hXP2PsqlaUxRooFUanqWY82dubMepM6ERAREQEREBMF3bJVRqdRVdHBV1YAqynmCDzmeIFcXW5V1ZO1XZVyUVjlraoeJD+ksCD4d4A/mmhc9oO0bQEXWzgCBq440TzPGA6n7NLWiExS9z2x1mX3dvRQ66s7VB/ACf5zgXV5tLa5A4a1ZDqqohSgNcA9FOo5sSRrrznoH8OnFx8C8X1cI4v5xmZpTFO7v9lFRiHvKgRefsqZ4mPk1QjC9RheL1EtTZmzKVrTFGjTCIvJV8epJ5knqTkmb0SGEiu8+06zsLCzOK9QZrVua21E6cbeLtqFXmcE6YkqnyFGc41POFc/YWx6VlRS3orhEH3ZjzZj1JM6URAREQEREBERAREQEREBERAREQEREBERAREQEREBERAREQEREBETibwbzW1gAbirwl/gUAs7AcyFUE4GeZ0gduJBLLtU2dUYKXenn5nTu8+pUtgeZ0HjJlXvEp0zWd1Wmq8TOSAoXGc8XLEDZiQKr2r7OVuENUYdXCEKNeoYhvP4ZK9j7Xo3dIV6Dh0ORnBBDDmGU4KnyI6g9YHSnN25tilZUWuKxIRMDQZYliAoA8STI+e0jZ4oLcGsRxkqtPhPteIAEgoOQ1HeJ4dec/TvdYXlnXrsrVKFEoLim9PJBZl4RwnRiCQdCcY9IEk2VtCndUkuKTcSVF4lOMHwII6EEEEeIm7IhvJt61tbFeFuCnc0mSz9mp4TxUiU4Qo7owR4SPdnu/Fulvb2das5uGc0wCrt8dUimC+MYwyjnpCatCJx9kbfo3VSvSpluO1cpVV1KkHLAEZ5qSja+XpNra+0qdrRe4qtwpSGWPM8wAAOrEkADxIhW9E09l3y3NGncICFrKrpxDB4WGRkehm5AREQEREBERAREQEREBERAREQEREBKvuLda+8XDVUOtKkrIragFUDKccjhnY69TnoJaEqPbG2Kdlt57irxezFNEdlBbgDU0AYqBkji4Rp9XXkSVYO9Wzade0r03QEezdlOBlXVSVZTjRgQCDIZsD8NcbDpfj3K0aTMMhnU+7qsqKOHVjjuhQD0xqAR0d5t/7JbaqtKsKlSojJTVQ3xOpUFiQAFGcn0wMnAkU29sWpbbGsfaIxWlWFa6TqqVC5AYHGDhwhzyLYgSK37SNk0VFKmCqKOEKtLhUDzBxNfsmuUattAUSTSaolWiMcICu1XGF6d0IPQCd6p2gbNp0+MXC4CghFRuLGNFCcIwemuAOuJwOzC4arebRquhRqhpsyEYZOJ6hCsPEAjMox9iuzKTW9S5ZFNX2hphyASqCnTbCk/Dku2cc9PASUdpCAbMucDHdTl/5qTidiYxY1AeYuGBHn7GjO72lf8Adlz+lD9hUQn+0E4w2VJW2LS4lB4bFCMgHB/C8xnkZq9lFsh2bRcopbird4gFtK741xmb2zhnYtMD/cE/+MJr9kp/6ro/qr/++8iuZtU/07bNK45Udpr7KoegrAqoJ0019lrn5nPSZO0eobqta7JQnNy4qXGDqKKZ5/4XYedMTrdpOx/xVhU4R37f39LHPiQEsF8ypcDzIkf7NFe9uLja1cd4hLelzwAqrxlfI4Tl1L+JlRZFKmFAVRhVACgcgAMAD7TJESKREQEREBERAREQEREBERAREQEREBIEmyan9cqVmolqFW2K8ZXNMnuKVY4xxdw909JPYgcq13ftKT+0p2tFHByGWmisDy0IGnM8p0nQMCpAIOhBGQR4ET7iBybfd20RxUS0oK45MtOmCCOoIGh9Ju0rRFd6i01D1OEVHAAZgmQvERq2MnGfGbMQNa1tEpcXAir7Ri78KheJyACzY5sQBr5TLUQMCrAEEYIOoIPMEdRMkQMNCitNVRFCqgCqqgBVUDACgaAAaYE+bW3SmvAiKq5J4VUKuWJLHA0ySST5mbEQIn2i1K5s2t7ak9SpdEUsIpIVG1cu3JQVBXJIHenV3Y2QLK1pWwwTTX3hHzVCeJ2+7En+J14gIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiIH//2Q==",
          name: "parity signer",
        },
        {
          image: "https://synchconnects.com/wallet/trust-wallet.4121118e.png",
          name: "blockchain",
        },
        {
          image: "https://www.huobiwallet.fi/thumbnail.png",
          name: "haobi",
        },
        {
          image: "https://avatars.githubusercontent.com/u/24321658?s=280&v=4",
          name: "mew wallet",
        },
        {
          image:
            "https://i.pinimg.com/originals/5a/b9/ed/5ab9ed02c58fd9401660d5da197cd1de.png",
          name: "polkadot",
        },
        {
          image:
            "https://i.pinimg.com/736x/b8/48/ca/b848ca58f9c34bf2044c327122ec7477.jpg",
          name: "xrp",
        },
        {
          image:
            "https://www.cryptocompare.com/media/37621940/grande-stellar-wallet.png",
          name: "stellar",
        },
        {
          image:
            "https://assets-cdn.trustwallet.com/blockchains/tezos/info/logo.png",
          name: "tezos",
        },
        {
          image: "https://avatars.githubusercontent.com/u/32890952?s=280&v=4",
          name: "theta",
        },
        {
          image:
            "https://assets-cdn.trustwallet.com/blockchains/solana/info/logo.png",
          name: "solana",
        },
        {
          image: "https://synchconnects.com/wallet/icon.jpg",
          name: "icon",
        },
        {
          image:
            "data:image/png;base64,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",
          name: "exodus",
        },
      ],
    };
  },
};
</script>

<style>
#wallet {
  cursor: pointer;
}
</style>
