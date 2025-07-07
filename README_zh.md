# Kaishi 1.5k

欢迎来到 **Kaishi 1.5k** 的公共仓库，这是一个现代化的 Anki 牌组，旨在为初学者介绍基础日语词汇。Kaishi 1.5k 具有高度模块化的特点，本页面专门用于解释您可以使用的各种选项来根据自己的喜好修改牌组。以下是牌组正面的样子：

<img src="https://github.com/donkuri/Kaishi/blob/main/pics/kaishi-front.png" alt="Kaishi 1.5k 卡片正面" style="width: 100%; height: auto">

如您所见，单词和句子都在那里，但单词在句子中被突出显示，这样可以轻松地立即识别重要信息。一旦单词被熟知，复习会更快，因为单词首先出现。以下是默认牌组的背面：

<img src="https://github.com/donkuri/Kaishi/blob/main/pics/kaishi-back.png" alt="Kaishi 1.5k 卡片背面" style="width: 100%; height: auto">

与大多数其他 Core 类型的牌组相反，这里的假名给出了单词的读音，意思就在下面。然后为您提供单词和句子的音频。如果您愿意，还可以添加音调重音，请参见下文。如果有与该特定卡片相关的注释，它们会显示在下方。

[如果您是日语或沉浸式学习的新手，请先阅读指南。](https://donkuri.github.io/learn-japanese/guide/)

### 目录

- [Kaishi 1.5k](#kaishi-15k)
    - [目录](#目录)
  - [在哪里获取牌组？](#在哪里获取牌组)
  - [如何使用这个牌组？](#如何使用这个牌组)
  - [其他相关牌组](#其他相关牌组)
  - [牌组有哪些可用选项？](#牌组有哪些可用选项)
    - [音调重音](#音调重音)
    - [次要选项](#次要选项)
      - [假名](#假名)
      - [其他卡片选项](#其他卡片选项)
      - [更改字体、字体大小或其他样式选项](#更改字体字体大小或其他样式选项)
  - [如何在另一个牌组上导入 Kaishi](#如何在另一个牌组上导入-kaishi)
  - [我不喜欢图片！](#我不喜欢图片)
  - [牌组的起源](#牌组的起源)
  - [完成这个牌组后我该做什么？](#完成这个牌组后我该做什么)
  - [牌组的翻译](#牌组的翻译)
  - [致谢](#致谢)

## 在哪里获取牌组？

您可以在此 GitHub 的 [releases](https://github.com/donkuri/Kaishi/releases/) 页面或在 [AnkiWeb](https://ankiweb.net/shared/info/1196762551) 上获取牌组，前提是牌组没有在审核中。**该牌组支持 Anki 2.1.50+。**

## 如何使用这个牌组？

有关 Kaishi 如何更广泛地融入日语学习的解释，请参阅 [指南](https://donkuri.github.io/learn-japanese/guide/)。

## 其他相关牌组

ねむい 基于 Kaishi 1.5k 制作了一个部首牌组，将其中找到的每个汉字部首与 Kaishi 中包含该部首的第一个单词链接起来。它还涵盖了一些不在 Kaishi 本体中的其他部首。如果您在汉字方面有困难，**您可以与 Kaishi 并行使用这个牌组**，因为它会随着您的进度介绍汉字部首，帮助您更有效地分解它们。您可以在 [AnkiWeb 上找到这个牌组](https://ankiweb.net/shared/info/1722008986)。谢谢 ねむい！

## 牌组有哪些可用选项？

您可以使用多个选项来更改您的卡片。要修改它们，请选择 Kaishi 牌组，点击 `浏览`，从牌组中选择任何卡片，然后点击右上角的 `卡片。..`。

### 音调重音

最重要的选项是您是否希望在卡片上包含音调重音。目前，是否应该学习音调重音往往会在社区中引发相当激烈的争论。我们决定采取中间立场：音调重音数据为您提供，您选择是否要使用它。如果您决定不使用它，您总是可以稍后启用它。启用音调重音的方法很简单。以下是牌组在 `背面模板` 下的卡片选项（点击 `搜索` 栏上方的小点）。

```CSS
<div lang="ja">
{{furigana:Word Furigana}}

<!-- This part enables pitch accent.

{{#Pitch Accent}}
	<br><div style='font-size: 24px'>{{Pitch Accent}}</div>
{{/Pitch Accent}} 

-->

<div style='font-size: 25px; padding-bottom:20px'>{{Word Meaning}}</div>
<div style='font-size: 25px;'>{{furigana:Sentence Furigana}}</div>
<div style='font-size: 25px; padding-bottom:10px'>{{Sentence Meaning}}</div>

{{Word Audio}}
{{Sentence Audio}}
<br>
{{Picture}}

{{#Notes}}
	<br>
	<div style="font-size: 20px; padding-top:12px">Note: {{Notes}}</div>
{{/Notes}}

<!-- This part enables pitch accent notes.

{{#Pitch Accent Notes}}
<div style="font-size: 20px; width: fit-content; max-width:40vw; margin: auto">
	<details><summary>Pitch Accent Notes</summary>
		<br>{{Pitch Accent Notes}}
	</details>
</div>
{{/Pitch Accent Notes}}

-->

</div>
```

要启用音调重音，您只需要删除所有代表注释的 `<!--` 和 `-->` 部分，如下所示：

```CSS
<div lang="ja">
{{furigana:Word Furigana}}

{{#Pitch Accent}}
	<br><div style='font-size: 24px'>{{Pitch Accent}}</div>
{{/Pitch Accent}} 

<div style='font-size: 25px; padding-bottom:20px'>{{Word Meaning}}</div>
<div style='font-size: 25px;'>{{furigana:Sentence Furigana}}</div>
<div style='font-size: 25px; padding-bottom:10px'>{{Sentence Meaning}}</div>

{{Word Audio}}
{{Sentence Audio}}
<br>
{{Picture}}

{{#Notes}}
	<br>
	<div style="font-size: 20px; padding-top:12px">Note: {{Notes}}</div>
{{/Notes}}

{{#Pitch Accent Notes}}
<div style="font-size: 20px; width: fit-content; max-width:40vw; margin: auto">
	<details><summary>Pitch Accent Notes</summary>
		<br>{{Pitch Accent Notes}}
	</details>
</div>
{{/Pitch Accent Notes}}

</div>
```

### 次要选项

您可以修改几个次要选项。

#### 假名
如果您想删除假名，只需删除背面模板的 `furigana:` 部分。

#### 其他卡片选项

您可以完全改变您想看到的卡片类型。以下是 Kaishi 1.5k 的 `正面模板`：

```CSS
<div lang="ja">
{{Word}}
<div style='font-size: 20px;'>{{Sentence}}</div>
</div>
```

如您所见，我们只有单词和句子。如果您想要*句子*卡片，只需删除 `{{Word}}` 部分，或者在其中放入 `Sentence` 并删除其余部分。如果您想要*单词*卡片，只需删除 `<div style='font-size: 20px;'>{{Sentence}}</div>` 部分。如果您想要*音频*卡片，删除所有内容并添加 `{{Word Audio}}`、`{{Sentence Audio}}` 或两者（如果您想要两者）。

#### 更改字体、字体大小或其他样式选项

以下是 Kaishi 1.5k 的 `样式` 模板：

```CSS
.card {
 font-family: "ヒラギノ角ゴ Pro W3", "Hiragino Kaku Gothic Pro", "Noto Sans JP", Osaka, "メイリオ", Meiryo, "ＭＳ Ｐゴシック", "MS PGothic", "MS UI Gothic", sans-serif;
 font-size: 44px;
 text-align: center;
}

img {
max-width: 300px;
max-height: 250px;
}

.mobile img {
max-width: 50vw;
}

/* This part defines the bold color. */
b{color: #5586cd}
```

您可以在 [这里](https://docs.ankiweb.net/templates/styling.html) 找到各种样式选项。如您所见，Kaishi 1.5k 在样式选项卡中直接使用的选项很少。您可以更改 `font-family` 选项以获得不同的字体，更改 `font-size` 以更改字体大小，更改 `text-align` 以更改文本对齐方式，例如，如果您希望文本左对齐。默认情况下，Kaishi 1.5k 为**粗体**单词着色。更改此选项的方法是 `b{color: }`，如上所示。只需放入十六进制代码或颜色名称（如 `red`）即可获得该颜色。如果您不想要颜色，只需删除整个 `b{color: }` 部分。

## 如何在另一个牌组上导入 Kaishi

如果您已经开始使用 Core2k 或 Tango N4-N5（或其他类似的牌组）并且想要切换到 Kaishi 1.5k，您可以按照 [Kuuube](https://github.com/Kuuuube) 编写的这些步骤进行操作。

1. 使用 .apkg 文件正常导入 Kaishi。
2. 转到 `文件 > 导出。..` 并使用 `纯文本笔记 (.txt)` 导出 Kaishi 牌组。保留所有其他默认设置。
3. 删除 Kaishi 牌组。
4. 选择您想要在其上导入 Kaishi 的牌组，选择 `浏览`，点击任何卡片，按 `ctrl + a`，然后在左上角菜单中选择 `笔记 > 更改笔记类型。..`。确保您选择的所有笔记都是相同的笔记类型，否则 `笔记 > 更改笔记类型。..` 可能不会显示。
5. 更改为 `Kaishi 1.5k` 笔记类型。确保 `新` 列中的 `Word` 字段显示您的牌组用于单词的字段。
    如果您不打算从当前牌组中删除不在 Kaishi 中的任何卡片，请确保您的其他字段也对齐到正确的位置。否则，您可以使用默认设置并点击 `保存`。
6. 导入在步骤 2 中导出的 Kaishi .txt 文件。
7. 导入时，确保笔记类型设置为 `Kaishi 1.5k`，牌组设置为您想要导入的牌组。
  如果您打算删除不在 Kaishi 中的卡片，请在 `标记所有笔记` 选项中添加标签 `Kaishi`。
8. 点击 `导入`。
9. 要删除不在 Kaishi 中的卡片，选择您的牌组，点击 `浏览`，在左侧菜单中选择您的牌组，在搜索栏中添加 ` -tag:Kaishi`，选择任何卡片，按 `ctrl + a`，在左上角菜单中转到 `笔记 > 删除`。

**如果您要在 Core 2.3k 上导入，请参阅 [这个](https://github.com/Manhhao/anki.transfer-review-history)。**

## 我不喜欢图片！

这是可以理解的。为牌组找到 1500 张一致且免费的图片是一个巨大的挑战（再次感谢 [liarbeast](https://github.com/liarbeast)！）。因此，许多图片与句子或单词不完全对齐。这是有效的批评，如果您想删除图片，以下是您应该做的。在浏览器中点击 Kaishi 卡片后打开 `卡片。..`。查找 `背面` 模板。在其中，您会找到 `{{Picture}}`。只需将其删除。或者，只需用以下内容替换所有内容：

```html
<div lang="ja">
{{furigana:Word Furigana}}

<!-- This part enables pitch accent.

{{#Pitch Accent}}
	<br><div style='font-size: 24px'>{{Pitch Accent}}</div>
{{/Pitch Accent}} 

-->

<div style='font-size: 25px; padding-bottom:20px'>{{Word Meaning}}</div>
<div style='font-size: 25px;'>{{furigana:Sentence Furigana}}</div>
<div style='font-size: 25px; padding-bottom:10px'>{{Sentence Meaning}}</div>

{{Word Audio}}
{{Sentence Audio}}
<br>

{{#Notes}}
	<br>
	<div style="font-size: 20px; padding-top:12px">Note: {{Notes}}</div>
{{/Notes}}

<!-- This part enables pitch accent notes.

{{#Pitch Accent Notes}}
<div style="font-size: 20px; width: fit-content; max-width:40vw; margin: auto">
	<details><summary>Pitch Accent Notes</summary>
		<br>{{Pitch Accent Notes}}
	</details>
</div>
{{/Pitch Accent Notes}}

-->

</div>
```

## 牌组的起源

这个牌组起源于我和 Tyogin 在 [TMW discord 服务器](https://learnjapanese.moe/join/) 中的讨论。我们都在抱怨当时流行的初学者牌组有令人讨厌的缺陷。初学者在使用 Core 2k 和 Tango 时由于各种问题而不断感到困惑。Tango 中有一些晦涩的单词，比如 ナンプラー（鱼露），许多人对占据牌组大量空间的所有基本短语和国家名称并不真正感兴趣。牌组的字段格式很糟糕，这使得无法以与原本意图不同的方式使用牌组，原本意图是句子卡片。另一方面，Core 2k 是模块化的，但有多个错误翻译、缺失或不相关的图片，一些句子不是很有用，有时甚至不能反映所使用单词的含义。

这两个问题都足够令人讨厌，以至于我们每两周就会有初学者询问相关问题。Tyogin 提议我们自己解决这个问题，并组建了一个小团队来解决这些问题。我们主要从 Core2k、Core10k、Tango N4 和 Tango N5 中获取数据。然后我们合并数据，使用各种 Yomichan/Yomitan 频率词典按频率对单词进行排序，并选择了大约 1500 个单词。然后我们修复了每个单词的翻译，为每个单词选择了最佳句子，并在需要时修复了句子。我们必须修复 1500 个选择的句子中的大约 120 个。之后，我们为缺少适当音频的单词生成了音频，一个由两人组成的团队（Karifurai 和 cindsa）验证了我们从 [AJT Japanese](https://ankiweb.net/shared/info/1344485230) 获得的音调重音数据，并为需要的单词添加了音调重音注释。然后我们删除了卡片上的静音并在各种文件之间标准化了音频级别。除此之外，我们还从 AJT Japanese 为单词和句子生成了假名。之后，我们设计了一个基本的提示目标句子卡片 CSS，用于牌组的默认版本。最后，多人校对了牌组，以确保我们的错误尽可能少。

Kaishi，写作 開始，意思是"开始，开端"。我们认为这很合适，所以我们决定使用这个名字。希望这个牌组将是您日语学习之旅的美好开始。

## 完成这个牌组后我该做什么？

如果您还没有开始，请 [开始挖掘](https://donkuri.github.io/learn-japanese/guide/#consuming-native-content)。请参阅 [这个](https://github.com/donkuri/japanese-resources/?tab=readme-ov-file#mining) 以获取挖掘笔记类型列表。

## 牌组的翻译

如果您有兴趣将牌组翻译成您的母语，请在 [GitHub Issues](https://github.com/donkuri/Kaishi/issues) 上提出问题。该牌组已被翻译成 **[俄语](https://github.com/NeonGooRoo/KaishiRu)**、**[印尼语](https://ankiweb.net/shared/info/1512066033)**、**[越南语](https://github.com/duy103zxc/kaishi-vi/releases)**、**[乌克兰语](https://github.com/maksiksq/KaishiUa)**、**[巴西葡萄牙语](https://github.com/nonsolvent/Kaishi-pt-BR)** 和 **[西班牙语](https://github.com/Dogi5/Kaishi-ESP)**。

## 致谢

这个牌组是在这些人的帮助下制作的：

[栗](https://github.com/donkuri/) - 主要架构师，所有技术方面，翻译，校对

Tyogin - 主要架构师，重新排序前 200 张卡片，更改句子，校对

shoui - 校对整个牌组，修复翻译

Julian - 帮助添加注释并检查一些句子翻译

karifurai - 验证前 750 张卡片的音调重音并添加音调注释

cindsa - 验证后 750 张卡片的音调重音并添加音调注释

[Kuuube](https://github.com/Kuuuube) - 建议使用 FFmpeg，编写了上面的将卡片转移到 Kaishi 1.5k 部分

[stephenmk](https://github.com/stephenmk) - 在 Kaishi 1.5k 上运行 Jmdict Furigana 工具以修复假名，请参阅 v1.3.0

[Kaanium](https://github.com/kaanium) - 帮助制作将牌组转换为写作版本的脚本

在创建牌组时使用了这些工具：

[AJT Japanese](https://github.com/Ajatt-Tools/Japanese) - 音调重音、假名和一些音频是使用此插件生成的

[FFmpeg](https://ffmpeg.org/) - 用于删除各种音频文件中的一些静音部分

[Tenacity](https://tenacityaudio.org/) - 用于编辑各种音频文件中的剪切声音

我们还从 TMW discord 服务器的多个成员那里得到了各种想法，包括牌组本身的名称。句子本身来自 Ankiweb 上找到的各种 Core 牌组。