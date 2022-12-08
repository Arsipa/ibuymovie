<template>
    <div class="dropdown">
        <div class="dropdown__visible">
            <p class="dropdown__title">{{ title }}</p>
            <div class="dropdown__arrow">
                <svg
                    width="10"
                    height="6"
                    viewBox="0 0 10 6"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg">
                    <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M1.60355 0.646447C1.40829 0.451184 1.09171 0.451184 0.896447 0.646447C0.701184 0.841709 0.701184 1.15829 0.896447 1.35355L4.64645 5.10355C4.84171 5.29882 5.15829 5.29882 5.35355 5.10355L9.10355 1.35355C9.29882 1.15829 9.29882 0.841709 9.10355 0.646447C8.90829 0.451184 8.59171 0.451184 8.39645 0.646447L5 4.04289L1.60355 0.646447Z"
                        fill="white" />
                </svg>
            </div>
        </div>
        <div class="dropdown__inner">
            <router-link v-for="item in dropdown" :to=item.to>
                {{ item.text }}
            </router-link>
        </div>
    </div>
</template>

<script>
export default {
    name: "Dropdown",
    props: {
        title: {
            type: String,
            required: true,
        },
        dropdown: {
            type: Array,
            required: true,
        },
    },
};
</script>

<style scoped>
.dropdown {
    position: relative;
}

.dropdown .dropdown__visible {
    cursor: default;
}
.dropdown .dropdown__arrow {
    position: absolute;
    transform: translate(-50%, 100%);
    bottom: 0px;
    left: 50%;
    z-index: 3;
    display: flex;
    width: 100%;
    align-items: flex-end;
    justify-content: center;
    height: 10px;
    transition: 0.3s;
}

.dropdown .dropdown__title{
    font-weight: bold;
    letter-spacing: 0.35px;
}

.dropdown .dropdown__inner {
    position: absolute;
    bottom: -6px;
    left: 50%;
    transform: translate(-50%, 100%);
    background: linear-gradient(0deg, #34a951 -28.7%, #1a5529 100%);
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 6px;
    box-shadow: 0.5px 2px 6px #00000029;
    border-radius: 8px;
    padding: 24px 22px 18px 0;
    transition: 0.3s;
    opacity: 0;
    visibility: hidden;
}

.dropdown:hover .dropdown__arrow
{
    height: 18px;
}

.dropdown .dropdown__visible:hover + .dropdown__inner,
.dropdown__inner:hover {
    z-index: 2;
    opacity: 1;
    visibility: visible;
}

.dropdown .dropdown__inner a {
    letter-spacing: 0px;
    font-size: 14px;
    transition: 0.3s;
    white-space: nowrap;
    position: relative;
    padding-left: 22px;
    width: 100%;
    color: inherit;
    font-weight: bold;
}
.dropdown .dropdown__inner a:hover {
    padding-left: 28px;
    opacity: 0.54;
}
.dropdown .dropdown__inner a:hover::before {
    content: "";
    width: 16px;
    height: 2px;
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
    background: white;
}
</style>
