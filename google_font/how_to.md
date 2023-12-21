## google フォントの使い方

1. @next/font をインストールします。
<pre>
npm install @next/font
</pre>
2. Google Fonts の Lato を App Router で使ってみる。
<pre>
// src/app/page.tsx

import { Lato } from 'next/font/google'

const Lato700 = Lato({
weight: '700',
preload: false,
})

export default function Home() {
return (
<>
<main>
<p>ここは Font が反映されません。</p>
<h4 className={Lato700.className}>ここは Font が反映されます。</h1>
</main>
</>
)
}

</pre>
