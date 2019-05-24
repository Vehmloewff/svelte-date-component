<script>
	export let mils;

	let res = 'working...';

	mapDate();

	function mapDate() {
		let then = (new Date().getTime() - mils) / 1000;

		if (then < 3) res = 'Just now'
		if (then > 3 && then < 59 ) res = `${Math.ceil(then)} seconds ago`
		if (then > 59 && then < 120) res = `About a miniute ago`

		then = (new Date().getTime() - mils) / 60000;


		if (then >= 2 && then < 61 ) res = `About ${ Math.ceil(then) } miniutes ago`

		then = (new Date().getTime() - mils) / (60000 * 60);


		if (then >= 1 && then < 2 ) res = `About an hour ago`
		if (then >= 2 && then < 24 ) res = `About ${ Math.ceil(then) } hours ago`

		then = (new Date().getTime() - mils) / ((60000 * 60 ) * 24);


		if (then >= 1 && then < 2 ) res = `About a day ago`
		if (then >= 2 && then < 7 ) res = `About ${ Math.ceil(then)} days ago`

		then = (new Date().getTime() - mils) / ((60000 * 60 ) * 24 * 7);


		if (then >= 1 && then < 2 ) res = `About a week ago`
		if (then >= 2 && then < 4 ) res = `About ${ Math.ceil(then)} weeks ago`

		then = (new Date().getTime() - mils) / ((60000 * 60 ) * 24 * 7 * 4);

		if (then >= 1 && then < 2 ) res = `About a month ago`
		if (then >= 1 && then < 12 ) res = `About ${ Math.ceil(then)} weeks ago`

		then = (new Date().getTime() - mils) / ((60000 * 60 ) * 24 * 7 * 52);

		if (then >= 1 && then < 2 ) res = `About a year ago`
		if (then >= 2) res = `About ${ Math.ceil(then)} years ago`
	}

	setInterval(mapDate, 1000)

</script>

{res}