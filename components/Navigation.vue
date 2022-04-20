<template>
    <div class="navigation">
        <amp-list
        width="auto"
        height="30"
        layout="fixed-height"
        src="/data/navigation.json"
        class="nav-responsive"
        v-html="listNavigation" />
    </div>
</template>

<script>
export default {
    data() {
    return {
      listNavigation: `
        <template type="amp-mustache">
            <div class="url-entry">
                <a href="{{url}}">
                    {{title}}
                </a>
            </div>
        </template>`
    }
  },
}
</script>

<style lang="scss">
    .navigation {
        margin: 10px 0px 0px 0px;
        .nav-responsive {
            @extend .display-flex;

            .url-entry {
                display: inline;
                margin: 5px 15px 0px 0px;

                a {
                    text-decoration: none;
                    color: $text-color-1;

                    &:hover {
                        color: $theme-color;
                    }
                }
            }
        }
        @media #{$sm-device} {
            .nav-responsive {
                &:first-of-type {
                    visibility: visible;
                }
                &:last-of-type {
                    visibility: hidden;
                }
            }
        }
    }
</style>