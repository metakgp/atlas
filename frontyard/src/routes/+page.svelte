<script>
	import Star from "@lucide/svelte/icons/star"
	import StarHalf from "@lucide/svelte/icons/star-half"

	let top_courses = $state([
		{ id: 43, name: "Information Security", code: "CSXXXXX", rating: 4.8 },
		{
			id: 12,
			name: "Information Insecurity",
			code: "CSXXXXX",
			rating: 4.2,
		},
		{ id: 11, name: "Course A", code: "AG01984", rating: 4.1 },
		{ id: 21, name: "Course D", code: "EX00451", rating: 3.4 },
	]);
</script>

<input placeholder="Search course name or code" class="main-search" autofocus />
<div class="top-courses container">
	<h2 class="title">Top Rated Courses</h2>

	<div class="course-list">
		{#each top_courses as course, i}
			<a class="course" href="/course?id={course.id}">
				<span class="rank">#{i + 1}</span><span class="name"
					>{course.name} ({course.code})</span
				>
				<div class="rating">
					{#each Array(Math.floor(course.rating))} <Star fill="#fdd835" strokeWidth="0" /> {/each}
					{#if (course.rating - Math.floor(course.rating) >= 0.5)} <StarHalf fill="#fdd835" strokeWidth="0" /> {/if}
					{course.rating}
				</div>
			</a>
		{/each}
	</div>
</div>

<div class="top-courses container">
	<h2 class="title">Top Course Notes</h2>

	<div class="course-list">
		{#each top_courses as course, i}
			<a class="course" href="/course?id={course.id}">
				<span class="rank">#{i + 1}</span><span class="name"
					>{course.name} ({course.code})</span
				>
				<div class="rating">
					{"⭐️".repeat(Math.round(course.rating))}
					{course.rating}
				</div>
			</a>
		{/each}
	</div>
</div>

<div class="top-courses container">
	<h2 class="title">New Courses</h2>

	<div class="course-list">
		{#each top_courses as course, i}
			<a class="course" href="/course?id={course.id}">
				<span class="rank">#{i + 1}</span><span class="name"
					>{course.name} ({course.code})</span
				>
				<div class="rating">
					{"⭐️".repeat(Math.round(course.rating))}
					{course.rating}
				</div>
			</a>
		{/each}
	</div>
</div>

<style>
	.main-search {
		width: 100%;

		outline: none;
		border: none;
		padding: 5px 0.8rem;
		box-sizing: border-box;
		border-radius: 5px;

		font-size: 1.5rem;

		&::placeholder {
			text-align: center;
		}
	}

	.course-list {
		display: flex;
		flex-direction: column;

		gap: 10px;
	}

	.course-list .course {
		background: white;
		border-radius: 10px;
		padding: 10px;

		text-decoration: none;
		color: var(--text-color);
		background-color: var(--surface-1);

		transition: outline 200ms;
		outline: 1px solid transparent;
	}

	.course-list .course:hover {
		outline: 1px solid var(--accent-color);
	}

	.course-list .course .rank {
		color: var(--accent-color);
		margin-right: 0.5rem;
		font-weight: bold;
	}

	.course-list .course .rating {
		display: flex;
		align-items: center;
		float: right;
	}
</style>
