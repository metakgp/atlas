<script>
	const course = {
		id: 21,
		name: "VLSI Engineering",
		code: "EC10104",
		rating: 4.2,
	};
</script>

<div class="container course-header surface-1">
	<h2 class="course-title">
		{course.name}
		({course.code})
	</h2>

	<div class="container row course-info">
		<div class="rating container-section">
			<h3>
				<div class="rating">
					{"⭐️".repeat(Math.round(course.rating))}
					{course.rating}
				</div>
			</h3>

			<div class="rating-scale">
				<progress class="rating-scale" value="95" max="100"></progress>
				<span>Course Load</span>
			</div>
			<div class="rating-scale">
				<progress class="rating-scale" value="90" max="100"></progress>
				<span>Interest</span>
			</div>
			<div class="rating-scale">
				<progress class="rating-scale" value="85" max="100"></progress>
				<span>Prof's Teaching</span>
			</div>
			<div class="rating-scale">
				<progress class="rating-scale" value="70" max="100"></progress>
				<span>Grading</span>
			</div>
		</div>

		<div class="quick-links container-section">
			<h3>Quick Links</h3>
		</div>
	</div>
</div>
<div class="container feedback">
	<h2>Student Feedback</h2>
</div>

<style>
	.course-header {
		.course-info {
			gap: 1rem;

			.rating {
				width: 70%;
			}
		}

		.course-title {
			text-align: center;
		}
	}

	.rating-scale {
		display: flex;
		align-items: center;
		gap: 10px;

		> progress {
			border: none;
			border-radius: 5px;
			height: 0.4rem;
			background-color: rgba(245, 222, 179, 0.8);

			&[value] {
				&::-moz-progress-bar,
				&::-webkit-progress-value {
					background-color: var(--accent-alternate);
				}
			}
		}
	}
</style>
