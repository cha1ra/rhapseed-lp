<script>


	import InformationCard from './components/InformationCard.svelte';
	import SectionTitle from './components/SectionTitle.svelte';
	import ServiceCard from './components/ServiceCard.svelte';
	import ProfileCard from './components/ProfileCard.svelte';
	import CompanyInfoTable from './components/CompanyInfoTable.svelte';
	import AppFooterBar from './components/AppFooterBar.svelte';

	const services = [
	  {
	    title: 'Webアプリ開発事業',
	    description: 'Webアプリ開発を請負開発しています。フルスクラッチの開発から、kintoneをはじめとしたプラットフォーム上でのカスタマイズまで幅広く対応しています。',
	  },
	  {
	    title: 'プログラミング教育事業',
	    description: 'プログラミング講師としてプログラミングスクールや企業様に対する教育事業を展開しています。',
	  },
	];
</script>

<main class="container px-2 md:px-0 mx-auto">
	<section class="mt-28 mb-14 md:mb-28">
		<div class="text-center text md:text-xl text-gray-600">
			発想を紡げば、新発見の"種"になる。
		</div>
		<div class="w-full md:w-1/2 mx-auto mb-16">
			<img src="logo.svg" alt="">
		</div>
		<div class="w-full px-4">
			<InformationCard />
		</div>
	</section>
	<section class="mb-14 md:mb-28">
		<div class="mb-4">
			<SectionTitle>
				事業内容
			</SectionTitle>
		</div>
		<div class="block md:flex px-4">
			{#each services as service}
				<div class="md:w-1/3 md:px-3 mb-2">
					<ServiceCard {...service} />
				</div>
			{/each}
		</div>
	</section>
	<section class="mb-14 md:mb-28">
		<div class="mb-4">
			<SectionTitle>
				<span class="font-rb text-3xl">
					Rhapseed
				</span>
				 （ラプシード） について
			</SectionTitle>
		</div>
		<div class="mb-4 p-4">
			<p class="mb-2">
				Rhapseed は Rhapsody(狂詩曲)に由来して命名しました。
				Rhapsodyとは raptein(縫い合わす) と ode(詩) が語源とされ、
				転じてある一定の形式に縛られることなく様々な曲調のフレーズを紡いで1つの作品とする手法を指します。
			</p>
			<p class="mb-2">
				実は、これは、新しい価値を生み出すための作業と同じことをしているのです。
				一見すると全く無関係に思える複数のアイデアをつなげることで、新しい価値は生まれます。
				違う思考やアイデアの"種"を排除するのではなく、面白がる。そして、自分の持っている種と繋げてあっと言わせる作品を生み出す。
			</p>
			<p class="mb-2">
				Rhapseedはその体現者集団であり続けます。
			</p>
		</div>
	</section>
	<section class="mb-14 md:mb-28">
		<div class="mb-4">
			<SectionTitle>
				代表者紹介
			</SectionTitle>
		</div>
		<div class="p-4">
			<ProfileCard />
		</div>
	</section>
	<section class="mb-14 md:mb-28">
		<div class="mb-4">
			<SectionTitle>
				詳細情報・お問い合わせ
			</SectionTitle>
		</div>
		<div class="p-4 w-full md:w-1/2">
			<div class="mb-6">
				<CompanyInfoTable />
			</div>
			<div>
				<p class="text-sm mb-4">
					お仕事の依頼やご質問事項がございましたら下記お問い合わせフォーム、または
					<a href="https://twitter.com/chamenma" target="_blank">TwitterのDM</a>
					経由でお知らせください。近日中にお返信いたします。
				</p>
				<a
					href="https://forms.gle/snCDtUoExZfEQBLq6"
					target="_blank"
					style="text-decoration: none; color:#fafafa"
					class="text-white bg-red-700 rounded py-3 px-6 no-underline rounded shadow"
				>
					お問い合わせフォーム <span class="text-xs">(外部リンク)</span>
				</a>
			</div>
		</div>
	</section>
</main>
<AppFooterBar />


<style global lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
</style>
