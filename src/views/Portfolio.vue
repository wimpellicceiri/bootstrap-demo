<template>
  <main class="container-fluid mt-5">
    <div class="row">
      <div
        v-for="(item, index) in portfolio"
        :key="index"
        class="col-md-6 col-lg-4"
      >
        <portfolio-card :item="item" :id="`card-${index}`" />
      </div>
    </div>
  </main>
</template>

<script>
import PortfolioCard from "../components/PortfolioCard.vue";
export default {
  name: "Portfolio",
  components: {
    PortfolioCard,
  },
  data() {
    return {
      portfolio: [
        {
          imgSrc:
            "https://lh3.googleusercontent.com/2M4hcbf6HBcnlOOVZWGi7nn_Ma_Jvrfldvux7MOJsGz3i6qf_W-fcyvTobJIV1GdLXBJXT06or8BxliPH3TqO7XlIUcMQ4xj7dmLEMduOqlO8VW6vkF-nTW2coW08hjjItcoosHH3bzgtSVsN3IzoA_gDsYB_ErPeNoiFnWb4CpPLoV9Zk5_N_-9Z_UpO6UnZucvXJXJBx5H1elPlaFxxFCEBh4zcE-xdZIA8uhlSjgOaGU55F9_7vfPr4_kV1i59A3kcia_h2XP2odSFMqaYbu83njkgaJ9hVhdp92kUwfvgYP_pWyes0Hr-BqtS6hXcIUTNDejIKK4tC6wQ4qFXkoxRpe7Axsa7OjgoKvZNJJosZMONnY9ZN-Rj4OQypLQ22OH1Y4czJ42y8gjyWmNbrlzELL2x5Iya8eQ5wP3_W_LTrEoNDZFq7BMMGeH1z0cnnGAVoh5b2pnx_OGnu4S6EqZ-o0yMzhTzVYQFicSJ8TBtnFCHr64amK7Q99JT_jt2hjKriNyQhnai2LQ7G-Hhcnhg9SAkbMwKJ_wkp_akyIiLdXUb3uv7iUjVXQfSJdUueX6c_tuk6aqFSB5k4ygpbuCd6WvreEZk_qx2kWhFALGHJ_RNfmbGKZubx5jmu6IAMhmuiWwogDV3bwdGifWlQzYOw5TcfojxxC0QuFzNbm8IUQUIgWWeulz_kkh3T-lucM_S8bNpl4uOiYg1Z0irBk=w1080-h810-no?authuser=1",
          text: "Sioux Falls, SD",
          gallerySize: 12,
        },
        {
          imgSrc:
            "https://lh3.googleusercontent.com/G8Flma9UEd6z9pDMCm8Kvj5Mkzd4kz5bTJI8OlZkOtASuFFeo46eOnYN_JJ20vnTrMUe42pSFjKrdpLQdkFxxJx-JSReSN34MB-rqlwifFZrHT9B0_2xSrp0296QE6vCQayLhuaLfQRdxEQOXdMJJYAd0TxPh0AApHVmVdpejW_X8KT98YWo_72t13kmzv7jiAxonHhZVq6Y0CfEto110HCXQGoim0VxRzieK6E-8aKlz6-sliX9FAsgU4LSYRxKeWFnipdSxW7n8k-4NCxnD7m3lggMi3KR2e61WFZJP2wmhNIhWA-PWLRZZA-r6RSFVKOuwsCpGpSw-vksZVhIgKZTfNaVPppaA1M_XsiDL0YydkCv03sjkszDXTZjAydNH4p9e07XhL-2tfIDJkGXag4Ofgp8zcgnsxuBHVHkF_nDl7WrbCflO8L7VBB2WHthLU_f4ZvXmve6eZ2dkfPq7_M-Sj2Lh0JWqRjykyGC_rF_PgVnDR1w-kavId4yUk0UHqu7uARW01blHrHKzd_WP1BWvw1I3kQuVasADUzAiziNiOwn5qF9OX90BdK1SLARztj1QNWIoJ8qUFj0JAIELgd_IRjPOTSnJhbo93DM6LWMPZc7l3ng_mWTjrRaWhJBAN9bcMNOfAzZgXz5zsjcVPMK91nUuUF6OJLZHfJe8uxYfEQspOtOZcjjt-Cf6IA5AKBvl2daPnkEUIJKnGN35nA=w1080-h810-no?authuser=1",
          text: "Badlands National Park",
          gallerySize: 32,
        },
        {
          imgSrc:
            "https://lh3.googleusercontent.com/YustvMTUlryXVwTUwUTL4WuEWpkviNX2F23c0duEYN_SCfa8fcwnoU3RMJJqd2A8E3dzAs3ggqCJk78espA8dMPRFP7I5OsnZGtak_rPQD9tUiQ4FAwE9CVgfMJHGDinvIiDjf-ALHzsIyazQJoRD4hNaxexRJvG2x-aeh70QZjeHVuzUomnRdNq2Uw1NTHBo11lQRt1WaSVlk8_gskXKNBQLebnZcrjIdIImgnZHtgx7afNmwFe73X9UeiIjPdOZkVdniCGjUcpYLKnQ_arFESzNzhemljiWrK3yDI7pjCV0azkt_rWDQp6gmcRTSUJZT9TQPeHn-b30kiWV82Viz7Q_fks26nxNpY4UTmKrC5MOCx5e1adddMXXQtEzZa_dIL3dF2lieqO-InBybCtSstQ7t1J7Nvum2ZmDYyRqd1kIdI9KPdNkHBKVEE2lO949-OjXtJqlDOhZYaxMvuR1FR0M2VCeU6o8YrLQkkgP0JTjEPRFL_xxgDp_DnZe1qjhzhkpcmfQD5-4YDUrIv5XcxObCMKi9VFyqbkaMGeY4B9JznqNFhBu6jLMckZc2l3WaOpfUkfL3epRhWYKbeIeW05cpTE28KXBqZogf-rbGI5zVuaDuZ2HbFixt8lICWTRjB9uyOaogaVCSIv1DfI58_IgZQds3Lnc7M87Cn_5Q_GwDzWmA48uUUcy9jLODhlt2wJIZoQq9bP7pbr6emk8fc=w1080-h810-no?authuser=1",
          text: "Black Hills National Forest",
          gallerySize: 82,
        },
        {
          imgSrc:
            "https://lh3.googleusercontent.com/uhOr5K7ZNNGsdmU-0O-yhTldcpNO6FOW5AadQorR4Jr1K2wSC7fTOrjWgMWnX1DOsrzOU7VYR1o3ORICbhVY3ixm7halafD0mKHuR0UE7pJpL45hcfvrugse99c3Sj-JvNQhCigpEzVU49gUBvcNiBHRkXtT-74xzu2IxBQ8PeDlRA3Z0x9UKIwn3aMrYuWXoBxxJ0nc8yzKbgqc2d-J-GzkTdUGIgBb_PVr4ierNrZjtovIYhIPF6StDm5o5PgNXtm_uHl7A6mGQfLC6aV9wMmwMRZB4nbr9D0ayha9ANTBplwVaRcpeE6xj-92VIB0g_gxCPqjolmVm6UKC6dsscekJGaKOOe2QlAB71pvOGocCEHXYKLG3ycEIHLRhNGqWAVEqypSakcwBDoGyCR50GHzlWIsHpR-6kEfpWg68SCy15BWZLjCADFp1-WRSWE7IK1tXZfRhJ9nUD_6Df80rpVrtI-biUR2rjN6VMDKfFQm4arxpazdizrKZMJkzd3HPvKBSK5K9wIlnX8IG1i_1gHMOq-DeQ-ijyeemDRbMT-q0zxAE3KtZCtNZdLfBZfXszVJ-CaV2MbkY3CArINqDhMhrMRGkiVnYzpzPj0OHT_tZMyz5mcYp-K8zWeAKS_wvP3VFbP2-Il4ECdxF-1zZGvVsKc8xMJz8gpGVpZDsyxwd_IJAvfRJwI3xDXxp7jMQtQe4fefEZIujNI_9UxPhAo=w1080-h810-no?authuser=1",
          text: "Dolly Sods Wildnerness Area",
          gallerySize: 44,
        },
        {
          imgSrc:
            "https://lh3.googleusercontent.com/iZ4qwsQs4_nMeBTXGUr9C5cGplRjfTheahFN67z46Rh_RB1ZEdMGvHdZtR9LOdmDd9h-LuLnR8xwy8NJmBtTsHj8AO8-0szPllFRMjNmlyV83srpTNa3GDidCQHw8NcOBA4P9jspkUtDoSGilR7qLVfvKsXMXvRguSTXPhqIxg9MRyCoCkrOKE4UGKvycFQT7JJ3mky56F_ad-S75LMDQNQjzCC1RuHERH2kC2tZLvrMgitFfkOx9OkqkgCnDKQffY9b0Dix4qGH0ZLMLoZPASm10mve0GLZeg3pHEY0sLYcF-1FD0B8bx2Z3bMZ4px0ZTRpOl3U2yokzk_sGcIQeYVHL0KRmY2fILwOfxS7bxfZvs0FeYLYiFXfNpnIaQFuOEDpK-XXe6CltEYiJOzlYUHnnKV5PwrF4G9xtyyF-Mgfpls_9FsxmT9V-vCTX5A0418UsYZrUvccTH9YdNPiARvl1WnctmRFaThWV3bICtbrJxp4M1acBCdaKUu71iZ9kooqocV7x9XZv3wlyoYKRkrn1CjShe02u5TYm5aN4cC2o0SoZHXyrQ8aKpf9jdXa7nGpS-3ykTMmpL_EmgkQUIo8CHiqrI4JHRIqfazgjOFH818iK0N9dt_DTbR-ho7pQvB8pnSyxmuuv0X0i1Ut9gBFenAN0wR2SMMkTiD7P5d8iD4sGKdQkqFFf4V5aMdIPR52hm8up2I3PBYA3Vq5apU=w1080-h810-no?authuser=1",
          text: "Sainte-Chapelle",
          gallerySize: 54,
        },
        {
          imgSrc:
            "https://lh3.googleusercontent.com/F7ia146yXd8DZlC8rp3MjhU7Sa_Uxx-PZho4dIAHRgNYgJ3D49tmZ1OppVpGR3GCmiFA8gPbePiAXIe1MNSBbDi3qxVm_Q1bEBTYISvfwCX1X1Qj9mjr-dSMrq2pc5yffLOs7VcVVUAaT0f1QF_AapKmbAkI7-8hH31OvQ0ou38sFlqw2GF5fjLvDW8FvU5lIsgygrZllv678qk_SPQbz_y2huQiaNnuseZvwyAUIaMruNFHd45XpeeikwI_eTGfVdwWv7RtQHxD1lTn0zleY_g3f3-GB8050bUhK6DWqFM7GmJ52EROeGcFQavXinAuhilQwXiZX-c6r81Yo2OTyILGeB_uBLx2FwYwoI1PZla9tQDiB4JRbDG5exkU6ejGl43_06RwIfrWHGxrmX6S7x_5so60rQjYR7Aswmookc2NE5aaauwhSyjLC0AqZg-RTMD5QhHEdrt1FgfPScxSVo4xrFWoYXb7iCBwq4H-YrmjS4J4vRy5_IxajOSH4PDbWzy4W6aWUdGWgG1x8TV3RjU-oRwN8KfChQ1iXY80Wm7L5UkvuaC4vaRcEt66wPb4CG4JB_nAtAqgBRjM4nxNik0a9NrFuiNcz8kBe9Sz7aMk7oj2WOoxBBE10fud1-u_9rM4RDckywtQumL7GkwxlkhHXuct3Cg76_uwtfgTGGtaQ69IDQ4LPfHnT68eoJv-ctE9BCKdk2zlHpoEAqhTNvA=w1080-h810-no?authuser=1",
          text: "Eiffel Tower",
          gallerySize: 93,
        },
        {
          imgSrc:
            "https://lh3.googleusercontent.com/AqZZz_Tqe7Z-ecJwt-duMz1u7MRZx3LNMk5HbwuIvpkC5wMBFthAAxg53FKJ3gOuKtoLFqgH7AlvZeh64MTzti_NCsaDu1kHusEjj9mszGE2JroBu1UN69gOGz38DrIxZ3QOoBv2dM-9Dy4yU3YrgC6nHi6M4-V5TtJYPORXUtHsJB1nepoFGTrxAa-mMfvV-CVMKPtBHeHvRUzDF6yAhSMp7OqFYg0w-IPgxIvv5nNE7GbU5Ncsvqhwh4ruZJZnnbyw4dGJ4-ajww5Yl9wVSJ875S5ariU80H1_biN1MGiiTvtspzHYx-zqtgSxyQoYQbfqss0MrE1xnm2kLSTh80syUrzixlEnhfKFYJWT7ZzJzPd-K1lzWyz-v6ZJdyvDJuJWtoC310dYBKyu2WIAlXUSVkWgY0GMynd658JgniIgFCZTa5B40gO5hNy9TKHG1QDriix-zSJhzcXnN7gOHAaZKXFv15gj4vvbCFgQLHlig_aBsiTCpJ-Cn0VczzWWcl52wSo4Ghvnhd3dk9aIsP-zsOWhmeH9x3NXUXQ_RBjZVR8F_8tPPmlOTccDXDrjwhYKvNWRxZKwWzjb8sFaMTKmXNp1kabHJjrJLd7eYdrudhTbEYoeT9eUnHZCuH9y2190O4VU_32R7bKjs9raTqk_rzPkqBskmIfIABCLJE6Z-8E3d3dwOnOnFqVGztLnRUqd7yAdnyD2ivbgyEXGEEA=w1080-h810-no?authuser=1",
          text: "France Countryside",
          gallerySize: 903,
        },
        {
          imgSrc:
            "https://lh3.googleusercontent.com/uWzHxzh6GHfjyoUrK47irJJ1KHXfuBTMgOCIPzKzdFii_dBLoOjgNxBn4F--wp2m6ORduZe4L2jcMaDOccdi4Y69XRAPZa20qj_Mgn8hwwzuP3ZYvPHf3Tdhov81YjfH7rPQtcxfEGR4xloEY0dXhyFWaEZ16FtBChAYBfqR3557NeS5QhzvBODssyekgOoex31taPqZ8WZx_0VQ3lB5a87FAIPieI1qLPCWjHxH2gjkgoTWUdm_PsN0VbBX5kd2ax5dXMp2S6nWxkSieleEXJclOLFJspUmrhqNc8PIaNI7VL1broEh3WlIIQc-dYnBqW_K1NUGam-rtgq8lxUDaIYWg1djqfhRzLmkmxISqlQffV1JUTyIekXzjnwAQVeQDhT_-q2-2gi5-oC6QLH_miRoyFVFt_YBowCxuXGFnHYblKirB0y3RatGD8SkFEe7WEFDWQV5kyK8QaXOvcroOlkX63wHmcj22nmBMDoPllWPyZcXkr7kz1EG5XeJd6nMWFOFZBTQyjxoC-NllhvFVpUz-pKFbC_sjKqe7gPMwaepdqTliq5S5sK49xS29Bzcr-E5uLDPjAEON72khpNs1QMrXOmsId9rCVXTuXSfT0cp3tu_0-VnMmAdpYqBQUxUhuPxQIpX29pLeQS-Yle90jcicJMHnjHE4hkBUzyQfxucZEdrlkKpuusRaYcq7GNLKndLUtwI5cJ8eNVfXi3We-g=w1080-h810-no?authuser=1",
          text: "Reynisfjara",
          gallerySize: 3,
        },
        {
          imgSrc:
            "https://lh3.googleusercontent.com/xfJcPQujlshqYV0qqXitAiV5aTlQOX25i-9ktn6uN6TYC04LTElHBDqdvt6nPhWHNEApY8MHxpuIEPP2kSKtdG6UvRg39f_BIP6bm08bJvGam1nhBmXl51zaVqsHHFPrnhWSs-huQW4iTB3Dx298N-TR2Kol5BsHP99KSqfIAgS-kRY4Q5rtoBMvPyS29GMf3YYbmzEYHo5nVdyD1FDTxhz0v5lx0oxEUnVwh9n4j96_O3zJWVT4s27o4JtwNgubBDCjLhNryVIb2LK2n9yYOsMZ_CzNFe9CfFW5V9gIdnmWUaRFXIsg0mf93O7JBTtr7yIPny6WvWZdH_ui-ALKmtkPOoqLI3-6SzFEHycYY4qV2epM-qhm2s1A2A3lMTMRMuaV-dE-JAdxGwnTPlt9wb2-Ie2xmA6P8sfwkqT3hLK92SsVUYf_fBSmjJvuMtGy5KWKqWbvRvKcchAcXxNlUMfsXjlqQMTJbKL41Utp1Aw9BWV_1tRdgSQpZtz12OuK6v0FYYGCmoPkABengveJQfLDK7JcFXswYa9xut42JwFkFAVtiDO1bFwYylXIRwJhrGahUGJ78i7tNlVfG7QDHR0gt7w_8BDBCWheVqaNypoeeXUC7tJ3M-8x_LJjR1fGqF15WCUNFqHTVErbN99Wu56q6e_-qDJ_tpopdmr62UkS6FKuAFdbioQHoxWUrtstfAYxUGEOFphic3j4gY6Zy84=w1078-h810-no?authuser=1",
          text: "Northern Lights",
          gallerySize: 4,
        },
      ],
    };
  },
};
</script>
