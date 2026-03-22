<script>
	let top_courses = $state([
		{id: 43, name: "Information Security", code: "CSXXXXX", rating: 4.8},
		{id: 12, name: "Information Insecurity", code: "CSXXXXX", rating: 4.2},
		{id: 11, name: "Course A", code: "AG01984", rating: 4.1},
		{id: 21, name: "Course D", code: "EX00451", rating: 3.4},
	])
</script>

<input placeholder="Search course name or code" class="main-search" autofocus />
<div class="top-courses container">
	<h2 class="title">Top Rated Courses</h2>

	<div class="course-list">
	{#each top_courses as course, i}
		<a class="course" href="/course?id=1">
			<span class="rank">#{i + 1}</span><span class="name">{course.name} ({course.code})</span>
			<div class="rating">{'⭐️'.repeat(Math.round(course.rating))} {course.rating}</div>
		</a>
	{/each}
	</div>
</div>

<div class="top-courses container">
	<h2 class="title">Top Course Notes</h2>

	<div class="course-list">
	{#each top_courses as course, i}
		<a class="course" href="/course?id=1">
			<span class="rank">#{i + 1}</span><span class="name">{course.name} ({course.code})</span>
			<div class="rating">{'⭐️'.repeat(Math.round(course.rating))} {course.rating}</div>
		</a>
	{/each}
	</div>
</div>


<div class="top-courses container">
	<h2 class="title">New Courses</h2>

	<div class="course-list">
	{#each top_courses as course, i}
		<a class="course" href="/course?id=1">
			<span class="rank">#{i + 1}</span><span class="name">{course.name} ({course.code})</span>
			<div class="rating">{'⭐️'.repeat(Math.round(course.rating))} {course.rating}</div>
		</a>
	{/each}
	</div>
</div>
