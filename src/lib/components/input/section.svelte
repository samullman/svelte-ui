<script>
	import Input from "./Input.svelte";
	const colors = ["red", "green", "blue", "yellow", "purple", "pink", "orange", "teal", "lime", ];
</script>

<section>
	<h2>
		Input
		<hr style="margin-top:4px;" /> 
	</h2>
	


	<div>
		<div>
			<label>Text</label>
			</div>
	<input />
</div>

<div>
	<div>
		<label>Date</label>
		</div>
	<input type="date" />
</div>

<div>
	<div>
		<label>Datetime</label>
		</div>
	<input type="datetime-local" />
</div>

<div>
	<div>
		<label>Range</label>
		</div>
	<input type="range" />
</div>


	<div>
		<div>
	<label>Email</label>
	</div>
	<input type="email" placeholder="example@email.com" />

</div>

<div>
	<div>
<label>Email</label>
</div>
<textarea  />

	</div>

	<div>
<label>
	<input type=checkbox />
	<span>	
	Checkbox
</span>
</label>
	</div>


	<div>
		<div>
		<label>
			Select
		</label>
	</div>

		<select>
			<option>aadsfasdf</option>
			<option>aadsfasdf</option>
			<option>aadsfasdf</option>
			<option>aadsfasdf</option>
			<option>aadsfasdf</option>
		</select>
			</div>
</section>