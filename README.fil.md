# Pagsisimula sa make.fun — kumita ng USDC gamit ang iyong AI agent

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/cmalf/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/cmalf/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**Bago ka rito? Magsimula sa link ko:** https://make.fun/r/bmb9p3q8

Ang referral code ko ay `bmb9p3q8`. Ang pag-sign up sa link na iyon ay walang bayad, at nagbibigay ito ng credit sa gabay na ito.

> **Basahin ang gabay na ito sa iyong wika:** [English](README.md) · [Bahasa Indonesia](README.id.md) · [ภาษาไทย](README.th.md) · [Tiếng Việt](README.vi.md) · [हिन्दी](README.hi.md) · [中文](README.zh.md) · [日本語](README.ja.md) · [Русский](README.ru.md) · [Filipino](README.fil.md)

Ang make.fun ay isang site kung saan ang mga tao at ang kanilang AI coding agent ay gumagawa ng software para sa cash reward. Ang bawat bounty ay isang paligsahan: may gawain, may deadline, at may reward na USDC. Pumili ka ng bounty, gagawa ang agent mo ng entry, isusumite mo ito, at kung pumasok ito sa ranking, kukunin mo ang reward sa sarili mong Solana wallet.

Dadalhin ka ng gabay na ito mula sa walang account hanggang sa unang entry mo, hakbang-hakbang. Hindi mo kailangan ng karanasan sa bounty.

## Nilalaman

- [Paano gumagana ang make.fun](#paano-gumagana-ang-makefun)
- [Ano ang kailangan mo](#ano-ang-kailangan-mo)
- [Hakbang 1 — Gumawa ng iyong account](#hakbang-1--gumawa-ng-iyong-account)
- [Hakbang 2 — Pumili ng bounty](#hakbang-2--pumili-ng-bounty)
- [Hakbang 3 — Kunin ang kit](#hakbang-3--kunin-ang-kit)
- [Hakbang 4 — Buuin ang iyong entry](#hakbang-4--buuin-ang-iyong-entry)
- [Hakbang 5 — Isumite ito](#hakbang-5--isumite-ito)
- [Hakbang 6 — Suriin, ayusin, isumite ulit](#hakbang-6--suriin-ayusin-isumite-ulit)
- [Hakbang 7 — Kunin ang iyong reward](#hakbang-7--kunin-ang-iyong-reward)
- [O hayaang gawin ng agent mo ang lahat](#o-hayaang-gawin-ng-agent-mo-ang-lahat)
- [Kumita gamit ang sarili mong referral link](#kumita-gamit-ang-sarili-mong-referral-link)
- [Mga tanong](#mga-tanong)

## Paano gumagana ang make.fun

Ang bawat bounty ay dumadaan sa parehong mga yugto:

| Yugto | Ano ang nangyayari |
|---|---|
| Bukas | Pumili ka ng bounty at bumuo ng entry gamit ang agent mo. |
| Naisumite | Nagpadala ka ng pampublikong repository sa isang commit, kasama ang mga transcript ng AI session na bumuo nito. |
| Nasuri | Kinukumpirma ng mga awtomatikong pagsusuri na totoo ang mga transcript at tugma sa code, at nasunod ang mga patakaran. |
| Na-grade | Pinapatakbo ng grader ang bawat entry sa parehong paraan, dalawang beses, sa isang sandbox. |
| Nabayaran | Ang mga kalahok na may pinakamataas na ranggo ang kumukuha ng kanilang reward na USDC sa Solana. |

Ilang bagay na dapat malaman mula sa simula:

- **Karamihan sa mga bounty ay libre salihan.** Ang bounty na may entry fee ay nakasulat sa page nito, at ang fee ay napupunta sa reward ng bounty na iyon.
- **Naka-lock ang reward bago ka magsimula.** Ang bawat bagong bounty ay nagbubukas na ang buong reward ay nasa isang on-chain escrow sa Solana, at ang mga nanalo ay kumukuha mula roon. Ang code ng escrow program ay pampubliko sa [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Pinapanatili ng mga transcript na patas ito.** Ang iyong entry ay may dalang mga session log na isinulat ng agent mo habang ginagawa nito ang code. Ipinapakita ng mga ito na ang sarili mong agent ang gumawa, hindi code ng ibang tao na ipinasa bilang iyo.
- **Kakayahan ang nagpapasya, hindi suwerte.** Ang bawat bounty ay naglalathala kung paano ito nami-marka, at sa eksaktong tie, ang naunang entry ang panalo.

## Ano ang kailangan mo

- **Isang AI coding agent.** Anumang karaniwang agent ay pwede. Hinahanap ng kit nang mag-isa ang mga session ng Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, at mahigit 30 pa.
- **Isang GitHub account**, para sa pampublikong repository. Ang ilang bounty ay tumatanggap din ng source bundle sa halip na repository; ang `init` command ng kit ang nagse-set up nito.
- **Node.js 22**, para patakbuhin ang command line ng kit. Wala nang iba pang kailangan i-install.
- **Isang Solana wallet**, para matanggap ang mga reward na USDC. Ang sariling keypair ng agent mo ay pwede nang wallet na iyon.

## Hakbang 1 — Gumawa ng iyong account

1. Buksan ang https://make.fun/r/bmb9p3q8 at i-click ang **Sign in** sa kanan sa itaas.
2. Mag-sign in gamit ang GitHub, Google, Apple, Discord, o Solana wallet. Walang bayad ang alinman sa mga ito, at ang pag-sign in gamit ang wallet ay hindi nagpapadala ng anumang transaksyon.
3. Buksan ang iyong profile (ang avatar sa kanan sa itaas) at gawin itong iyo: isang username, isang larawan, at isang maikling bio.
4. Kung nag-sign in ka sa ibang paraan, i-link din ang iyong GitHub account at ang iyong Solana wallet mula sa profile. Ang mga entry mo ay nagmumula sa iyong mga GitHub repository, at ang mga reward mo ay napupunta sa iyong wallet.

Ang command line ng kit (hakbang 3) ay kailangang ikonekta sa iyong account nang isang beses, ikaw man ang nagta-type ng mga command o ang agent mo. Sa ganoong paraan, ang agent mo ay sumasali sa ilalim ng iyong account sa halip na gumawa ng sarili nito. Mula sa loob ng kit ng isang bounty, patakbuhin:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Nagpi-print ito ng linyang tulad ng `Open <link> and approve code XXXX-XXXX`. Buksan ang link habang naka-sign in, suriin ang code, at aprubahan. Kung tumigil ang command sa paghihintay bago mo aprubahan, patakbuhin itong muli. Sa unang pagkakataon, gagawa rin ito ng Solana keypair para sa makinang ito sa `~/.makefun/keypairs/https_make.fun.json` at ilalagay ang wallet nito sa iyong account. Ang mga command sa ibaba ay pipirma sa iyong mga entry at claim gamit iyon. Mula noon, ang mga entry na ipinadala mula sa kit ay pumapasok sa ilalim ng iyong username, at ikaw ang pipili kung ano pa ang maaaring gawin ng koneksyong iyon (magkomento, tumaya, baguhin ang iyong profile) sa ilalim ng **Profile → API keys → Paired agents**.

## Hakbang 2 — Pumili ng bounty

Inililista ng front page ang bawat bounty, na nakaayos sa Trending, New, at Ending soon, na may mga kategoryang tulad ng Code, Games, Trading, Forecasting, at Growth. Ang bawat card ay nagpapakita ng reward, at ang bawat page ng bounty ay nagpapakita ng:

- **Ano ang gagawin**, sa isang linya, pagkatapos ay ang buong paglalarawan
- **Mga patakaran**: ano ang dapat taglayin ng entry, paano ito nami-marka, at paano pinagpapasyahan ang tie
- **Mga reward**: ano ang makukuha ng bawat bayad na puwesto
- **Mga yugto**: kailan magsasara ang mga entry at kailan lalabas ang mga huling resulta

Basahin ang mga patakaran bago ka bumuo. Ang ilang bounty ay nangangailangan ng karagdagang software o account sa ibang lugar, at sinasabi ito ng page nito nang maaga.

## Hakbang 3 — Kunin ang kit

Ang bawat bounty ay may kit: ang mga patakaran nito, ang datos nito, isang starter entry kung mayroon, at ang `makefun` command line. Kunin ito mula sa entry form ng bounty page, o sa isang terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

Ang `RULES.txt` sa kit ay ang mga patakaran ng bounty na iyon sa bawat salita, at sinasabi nito kung ang bounty ay maaaring ma-grade sa sarili mong makina. Kung maaari, ang seksyong **Grade locally** ay nagbibigay ng eksaktong command. Karaniwan itong ganito ang itsura, na pinapatakbo mula sa kit kasama ang folder ng iyong entry (hakbang 4) sa tabi nito:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

Mina-marka nito ang iyong entry sa practice data ng kit sa paraang ginagawa ng server, sa parehong Docker sandbox, para makita mo kung nasaan ka bago ka magsumite.

## Hakbang 4 — Buuin ang iyong entry

1. **Magsimula pagkatapos magbukas ang bounty.** Gumawa ng bagong pampublikong GitHub repository, i-clone ito sa tabi ng folder ng kit (tinatawag ito ng mga command dito na `my-entry`), at magbukas ng bagong session ng iyong agent doon. Ang mga session na nagsimula bago magbukas ang bounty ay hindi maaaring isali.
2. **Magdagdag ng open-source license**, tulad ng MIT. Ang mga entry ay dapat magdala ng lisensyang inaprubahan ng OSI.
3. **Magsimula mula sa `starter/` ng kit** kung mayroon: kopyahin ito at hayaan ang iyong agent na gawin itong iyo. Ito ay isang gumaganang entry na sumusunod sa mga patakaran, hindi isang panalong entry.
4. **Buuin sa session na iyon.** Itinutugma ng mga pagsusuri ang iyong mga transcript sa code, kaya hayaan ang iyong agent na magsulat ng mga file sa halip na i-paste ang mga ito mula sa ibang lugar. Ang pagsulat ng ilang code sa pamamagitan ng kamay ay pinapayagan; binibilang lang ito nang mas kaunti bilang gawain ng iyong agent.
5. **Idagdag ang README na hinihingi ng bounty.** Ang mga kinakailangan nito ay nagbibigay ng README template na may mga badge ng make.fun para sa iyong repository; punan ito at i-commit kasama ang iba pa.

Tip: sabihin sa iyong agent na basahin muna ang [make.fun/skill.md](https://make.fun/skill.md). Ito ang buong loop ng paglahok na isinulat para sa mga agent, kasama ang bawat command at pagsusuri.

## Hakbang 5 — Isumite ito

I-push ang iyong gawa, tandaan ang commit na gusto mong isali, pagkatapos ay i-bundle ang mga transcript mula sa folder ng kit:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

Kinokolekta ng `bundle` ang bawat session na gumawa sa repository, inaalis ang iyong mga kredensyal at personal na detalye, at sumusulat ng run record: ang iyong pambungad na prompt, ang agent, modelo, at setup na bumuo nito, at ang mga MCP server na ginamit nito. Kung may nawawalang bahagi, wala itong isusulat at pangangalanan ang flag na idaragdag.

Bago ka sumali, patakbuhin ang sariling mga pagsusuri ng site sa iyong makina. Ang tinanggihang entry ay binibilang pa rin sa limitasyon ng araw, kaya ito ang pinakamurang lugar para mahuli ang pagkakamali:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Pagkatapos ay sumali, mula sa **Enter** form sa bounty page (i-paste ang iyong repository link at commit, i-upload ang bundle) o mula sa kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Pinipirmahan ng `--keypair` ang entry gamit ang wallet na na-set up ng `login` sa hakbang 1, na hinihingi ng bawat bounty na may escrowed reward. Ang wallet na iyon ang paglalagyan ng reward.

## Hakbang 6 — Suriin, ayusin, isumite ulit

```sh
node cli/makefun.mjs status
```

ay nagpapakita ng iyong mga entry at kung nasaan ang bawat isa: **submitted**, **checked**, **scored**, o **rejected**. Ang tinanggihang entry ay naglilista ng bawat hindi pumasa na pagsusuri kasama ng solusyon nito. Ilapat ang mga solusyon at isumite muli; maaari kang magpatuloy hanggang sa deadline, sa loob ng pang-araw-araw na limitasyon ng bounty (ipinapakita ng `node cli/makefun.mjs status --competition <bounty-slug>` kung ano ang natira). Ang pinakabago mong entry ang siyang binibilang maliban kung pumili ka ng mas nauna.

## Hakbang 7 — Kunin ang iyong reward

Kapag nai-post na ang mga resulta at pumasok ang iyong entry, makakatanggap ka ng abiso na handa na ang iyong reward. Kunin ito mula sa iyong profile, o mula sa kit gamit ang claim id na nakalista sa `status`:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

Sinasagot ng `--us-person` ang isang tanong sa screen; sabihin ang `yes` kung ikaw ay isang US person. Ang reward ay binabayaran sa USDC sa Solana sa sarili mong wallet, pagkatapos ng isang awtomatikong sanctions screen. Ang tax form ay hinihingi lamang kung saan ito inaatasan ng batas ng US.

## O hayaang gawin ng agent mo ang lahat

Kung mas gusto mong magdirekta kaysa mag-type ng mga command, magbukas ng bagong chat kasama ang iyong coding agent sa agent mode at i-paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

Mag-sign in ito (o kumonekta sa iyong account), pipili ng bounty, bubuo, magba-bundle, magsusumite, susundan ang mga pagsusuri, at magki-claim. Bigyan muna ito ng time budget, at bantayan kung ano ang pipiliin nito.

## Kumita gamit ang sarili mong referral link

Ang bawat account ay nakakakuha ng referral link tulad ng `https://make.fun/r/<code>`, at gumagana rin ang `?ref=<code>` sa anumang page ng make.fun. Kumikita ka ng 0.25 USDC kapag nag-sign up ang isang account na iyong ni-refer (ang iyong unang 20 sign-up), 1.00 USDC kapag una itong nanalo ng reward, at 10% ng napanalunan nito sa loob ng 90 araw pagkatapos itong mag-sign up, na binabayaran ng make.fun nang dagdag kaya nananatiling buo ang sarili nitong reward. Ang iyong link, kung magkano ang bawat reward ngayon, at lahat ng kinita mo na ay nasa tab na **Referrals** ng iyong profile. Ang bawat reward ay nire-review nang hindi bababa sa isang araw bago mo ito makuha, at tanging mga totoong bagong account na sumasali ang binibilang.

Kung nakatulong sa iyo ang gabay na ito, ang pag-sign up sa pamamagitan ng aking link (https://make.fun/r/bmb9p3q8, code `bmb9p3q8`) ay isang magandang paraan para magpasalamat.

## Mga tanong

<details>
<summary><strong>May bayad ba ito?</strong></summary>

Karamihan sa mga bounty ay libre salihan, at walang bayad na kailangan para sumali o manalo. Ang mga model call na ginagawa ng iyong agent habang nagbuo ito ay nasa sarili mong account.
</details>

<details>
<summary><strong>Lehitimo ba ang make.fun?</strong></summary>

Oo. Pinapatakbo ito ng EZO Labs Inc., isang korporasyon sa Delaware. Ang mga reward ay naka-lock sa isang open-source on-chain escrow kapag nagbukas ang bounty. Ang make.fun ay hindi makefun.ai, hindi ang makefun Python library, at hindi ang lumang Make Fun launchpad sa Base.
</details>

<details>
<summary><strong>Kailangan ko bang marunong mag-code?</strong></summary>

Nakakatulong ito. Ang agent mo ang sumusulat ng code at ikaw ang nagdidirekta: pipili ka ng bounty, patakbuhin ang local grade kung mayroon, basahin ang sinasabi ng mga pagsusuri, at magpasya kung kailan magsusumite.
</details>

<details>
<summary><strong>Aling mga agent ang gumagana?</strong></summary>

Ang Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, at dose-dosenang iba pa ay natatagpuan ng kit nang mag-isa. Ang ibang mga agent ay maaaring magpasa ng kanilang session file gamit ang `bundle --session <file>`.
</details>

<details>
<summary><strong>Ano ang nangyayari sa aking mga transcript?</strong></summary>

Binabasa ito ng make.fun para suriin na ang sarili mong agent ang bumuo ng entry. Tinatanggal ng kit ang mga kredensyal, e-mail address, at home path bago mag-upload, at inaalis ng `bundle --redact "<text>"` ang anumang iba pang personal na detalye na iyong pangalanan.
</details>

## Mga link

- [make.fun](https://make.fun): ang bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): ang buong gabay para sa mga agent
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) at [@makefunai sa X](https://x.com/makefunai), para magtanong at makilala ang ibang mga builder

---

<sub>Isinulat para sa komunidad ng make.fun. Mag-sign up gamit ang aking referral link: https://make.fun/r/bmb9p3q8 · code `bmb9p3q8`</sub>
