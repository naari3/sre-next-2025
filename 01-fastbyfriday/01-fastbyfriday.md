# a

5 日以内にパフォーマンスを解決するには

3 アクティビティ

1. found: パフォーマンスの原因を知ること
2. fixed:
3. deployed

古くから、アポロ計画の時代からアラートというものがあった　ハードウェアに対する最適化しかやることがない

以後、ソフトウェアの時代になる、OS のメトリクスがいろいろ取れるようになる

カーネルの値などが見れるように

動的計装や、OSS で見ることができるようになるなど

次、 fast by friday

netflix では、「⭕️⭕️ するためのツールが必要だ」と頻繁に言われた

これをソリューションによって解決するというのがキーの解決方法

パフォーマンスは年々早くなっているわけではない

ボトルネックが見つからなかった、新しいはーどうぇあ・ソフトウェアオプションを調査する時間がない

prior week: preparation

quantify, static tuning, load
checklists, elimination
profiling
latency, logs, critical path
efficiency, algorithms

post week: casestudy, retrospective

# preparation

月曜日からできるように調整

ツール類が入っているべき、procps, sysstat, linux-tools-common, bcc-tools, bpftrace

スタックトレースとシンボルがほしい

トレーシングできるようにする

SSH root access

システムのダイアグラムをわかっているべき

ソースコードがある

crisis tools

# monday

パフォーマンスの問題を特定

problem statement method

static performance tuning

the system without load

check all hardware, software

load vs implementation ?

## monday, cont end of day status

# tuesday: checklists, elimination

recent issue checklist

ebpf

# wednesday: profiling

- flamegraph

# thursday: latency, logs, critical path

ebpftools だと、dist, slower, snoop, bpftrace という名前でそれぞれ見れる

critical path analysis

- zero instrumentation ツールである: when faster uprobes is done: crrent status: https://dont-ship.it

# friday: efficiency, algorithms

is the target efficient??

cycles/carbon per request

# post week: case study, retrospective

document as a case study

jira, wiki, gist, etc

(tensorflow library performance)

# what needs to change

トレースツールが health であること

crisis tools が最初からインストールされているべき

frame pointers が最初からコンパイルされているべき

# まとめ

月曜日に報告された全ての問題は金曜日までに解決されるべき

fixed by friday

1. don't do it
1. do it, but don't do it again
1. do it less
1. do it later
1. do it when they're not looking
1. do it concurrently
1. do it in cheaper

全員が関与する必要がある、一人ではできない

ちょっとずつ小さなステップを踏んでいこう
