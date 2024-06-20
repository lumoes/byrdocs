# BYR Docs Archive

**BYR Docs** 系北京邮电大学（下称“北邮”）校内资料分享平台，旨在使校内学生更方便地获取与北邮课程有关的教育资源，包括电子书籍、考试题目和复习资料等。

## 注意事项

> [!WARNING]
> **本项目仅面向北邮在校学生提供服务。** 如果您不是北邮在校学生，我们保留中止向您提供服务的权利。

> [!TIP]
> 欢迎加入QQ群 `829649976` 交流 BYR Docs 有关事项。

> [!NOTE]
> **请勿在 Issues 内请求资源。** 我们目前无暇处理大量的资源请求。

## 如何使用

您可以访问 [BYR Docs](https://byrdocs.org) 网站，搜索并获取您想要的资源。

![Screenshot_20240517_112259.png](https://s2.loli.net/2024/05/17/FMS2CTxUsDyRIGh.png)

您可使用关键词，诸如书名、作者、出版社、ISBN、科目、年份来查找您想要的文件。

![Screenshot_20240517_113156.png](https://s2.loli.net/2024/05/17/jscTgDpZeXJYhWB.png)

如果您找到了目标文件，点击文件的标题就可以开始下载了。

## BYR Docs 命名及分类规范

### 文件说明

所有文件均在录入元信息后，重命名为 MD5 码格式，如 `584397f272ee33d11491cf78011abee2.pdf`, `62b43f8fbed2bb3087f2afc96fd89b0f.zip`。

一般来说，文件库中只接受 `.pdf`, `.zip` 格式的文件。形如 `.epub`, `.docx`, `.pptx`, `.png` 格式的文件，应当先转换为 `.pdf` 格式。**不推荐使用 `.zip` 格式，除非有很特殊的理由（如，文件中含有代码；或者文件太过细碎，需要统一存储）。**

在整理时，有些资料应当进行合并或拆分。如，一份汇总了多年考试试题的大件资料，应当把每份试题单独拆出，作为一个文件；再如，若是明确某份试题与某份答案对应，就应当将其合并。

质量很差的文件应当删除，宁缺勿滥。

#### 文件分类原则

只有正式出版物才能归入 `books` 中。非出版物禁止归入 `books`。

只有北京邮电大学各课程历年考试真题才能归入 `tests` 中。其它模拟题、题库和试题资料禁止归入 `tests`。

粗略说来，凡不属于前两类的，均可归入 `docs` 中。但 `docs` 也并非来者不拒——比如以下资料，应当直接删除，不适合归入 `docs` 中。

- 无法对应到任何课程的资料，或本身不属于教育资源的资料，如网络小说、游戏安装包、北邮PPT模板等。
- 比赛真题，如大学生数学竞赛、大学生英语竞赛的历年题等。本项目不负责收录竞赛资料。
- 培养方案、通知、章程等。此类资料请在北邮官方网站下载。
- （其它不符合本项目宗旨的资料，待补充）

### 元信息说明

[metadata.ods](metadata.ods) 包含三个sheet，分条列明 `books`, `tests` 及 `docs` 文件之元信息。

#### `books`

一般来说，**中文书（包括外文书的中文翻译版）使用中文书名（如 `操作系统概念（原书第9版）`），外文书使用外文书名（如 `Calculus`）**，但有如下例外：

- 英语课/日语课等所用教科书，使用中文书名，如 `全新版大学英语综合教程学生用书2`。
- 由中方编著的国际学院外文教科书，使用双语书名，如 `线性代数/Linear Algebra`。

对于外文书的译著，还要涉及到如下细节：

1. 作者与译者在元信息中是分开列明的。
2. **译著的版本不等于原著的版本**。这种情况下，原著版本一般附在书名中，而译著版本对应在 `版次/年份` 一栏中。（P.S. 有些教材的配套用书版本通常也不等于原书版本，这种情况也将按相似方式处理）
3. `出版社`, `ISBN码` 两项全部是指译著的信息，不涉及原著信息。

关于 `ISBN码`，应**统一使用 ISBN-13 码**。有些外文书比较讲究，其 Print 版和 PDF 版有各自的 ISBN，这时**应统一使用 Print 版**；还有些外文书的 Bound 版和 Loose-leaf 版有各自的 ISBN，这时**应统一使用 Bound 版**。

部分思政类教材，其版次没有定规，加上思政类教材的年份信息远比版次信息直观、重要，所以对于此类教材，不记录其 `版次`，而是以 `出版年份` 来记录。但是，对于绝大多数资料来说，还是应当记录它的版次，而非出版年份。

#### `tests`

**`tests` 一表中不记录每份试题的标题，只记录 `考试年份`, `课程名称`, `考试阶段` 和资料类型信息。**

对于 `考试年份`，精确到某学年的某个学期，如 `2017-2018-2`。如果无法精确到学期，就只填学年，如 `2017-2018`。如果无法精确到某个学年，就只填某一年，如 `2018`。

`考试阶段` 只区分期中与期末，不区分正常考试与缓补考（因为基本无法分辨）。

`资料类型` 用以区分一份资料是纯试题、纯答案还是带答案的试题。

#### `docs`

此类文件比较杂乱，故整理时也须记录文件名称，以备后用。

任何一项资料都应当至少能对应到一门课程，否则它不应该被收录。

可以大致地把这些文件分为以下类型：

- `思维导图`：顾名思义。
- `题库`：是指不能归入 `tests` 或 `books` 中的题库、题集，如 `军事理论题库` 和 `线代绿书2018版`（一个非正式出版的线代题集）。
- `答案`：包括课后习题答案、作业答案、题集答案（如果对应的题集本身并无答案；否则，它应归入题集中）等。
- `知识点`：各种辅助学习资料或考试复习资料。
- `课件`：包括讲义、（非正式出版的）指导书、教学手册等与教学息息相关的资料。

## 其他事项

- 如果您有意参与本项目并愿意长期贡献，可发送邮件到 [contact@byrdocs.org](mailto:contact@byrdocs.org)。
- 感谢所有人直接或间接为本项目做出的贡献。本项目的资料来源十分杂乱，我们在此不一一列举。
- 我们不接受任何形式的捐赠。
