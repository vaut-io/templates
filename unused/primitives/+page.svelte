<script lang="ts">
	import {
		Box,
		Center,
		Cluster,
		Cover,
		Frame,
		Grid,
		Sidebar,
		Stack,
		Switcher
	} from '$lib/unused/primitives';
</script>

<Box>
	<Frame>
		<img src="/media/image.jpg" alt="">
	</Frame>
	<Center max="100rem">
		<Stack>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero ratione consequatur vero
				officia unde iusto necessitatibus commodi vel consectetur voluptate repudiandae dolore
				voluptates, neque nesciunt eligendi rerum officiis accusamus assumenda.
			</p>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero ratione consequatur vero
				officia unde iusto necessitatibus commodi vel consectetur voluptate repudiandae dolore
				voluptates, neque nesciunt eligendi rerum officiis accusamus assumenda.
			</p>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Libero ratione consequatur vero
				officia unde iusto necessitatibus commodi vel consectetur voluptate repudiandae dolore
				voluptates, neque nesciunt eligendi rerum officiis accusamus assumenda.
			</p>

			<Sidebar sideWidth="20rem">
				<p>I AM THE SIDE.</p>
				<p>I am not the side</p>
			</Sidebar>
			<Cluster list>
				<li>1</li>
				<li>2</li>
				<li>3</li>
			</Cluster>

			<Switcher>
				<p>
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Explicabo minus corrupti fugiat
					iure voluptas voluptatum consequatur saepe distinctio! Adipisci modi itaque officiis
					voluptatum illum sed ratione officia cumque accusamus eveniet.
				</p>
				<p>
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Explicabo minus corrupti fugiat
					iure voluptas voluptatum consequatur saepe distinctio! Adipisci modi itaque officiis
					voluptatum illum sed ratione officia cumque accusamus eveniet.
				</p>
				<p>
					Lorem ipsum dolor sit amet, consectetur adipisicing elit. Explicabo minus corrupti fugiat
					iure voluptas voluptatum consequatur saepe distinctio! Adipisci modi itaque officiis
					voluptatum illum sed ratione officia cumque accusamus eveniet.
				</p>
			</Switcher>
		</Stack>
	</Center>
</Box>
