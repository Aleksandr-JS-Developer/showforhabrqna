<template>

	<div class="footerContain">
		<div class="line"></div>
		<div class="copyright">
			©
			<a href="https://mail.google.com/mail/u/0/?tab=om#inbox?compose=CllgCHrgljwZRpXjNrvTSkgCLnPwzqrSdWkKwMNtFzHjCpsHVlLplGVvbjStzQRpNPbJjxRVljq"
				target="blank"
			>
				script@vip-person.net
			</a>
		</div>
	</div>

</template>

<script>

export default {
	name: 'Footer'
}

</script>

<style scoped>
	.footerContain {
		color: black !important;
		width: 310px;
		margin: 0 auto 15px;
		text-align: center;
		opacity: 0.5;
	}
	.line {
		height: 1px;
		width: 100%;
		background-color: black;
	}
	.copyright {
		margin-top: 10px;
		font-size: 12px;
		color: black;
		
	}
	a.text:active, /* активная/посещенная ссылка */
	a.text:hover,  /* при наведении */
	a.text {
		color: black;
		text-decoration: underline;
		text-decoration: none;
	}
	a:-webkit-any-link {
		color: black;
	}
</style>