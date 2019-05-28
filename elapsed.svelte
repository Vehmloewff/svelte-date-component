<script>
	export let mils;
	import userFriendlyDate from 'user-friendly-date';
	import dateFormatter from 'user-friendly-date-formatter';

	let res = userFriendlyDate(mils);

	setInterval(() => res = userFriendlyDate(mils), 1000);

</script>

<time datetime={new Date(mils)} title={dateFormatter(new Date(mils), '%fM %D, %YYYY at %h:%m %a')}>{res}</time>