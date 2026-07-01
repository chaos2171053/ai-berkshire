# 报告交付

当技能产出完整 Markdown 报告时，按下面流程收尾：

1. 先把完整正文写到本地临时 `.md` 文件。
2. 如该技能要求数据抽检，先对这份临时文件跑 `report_audit.py extract` 和 `verdict`。
3. 抽检通过后，把同一份正文交给 `preview skill`。
4. 处理结束后删除临时文件，不保留。
5. `report_audit.py` 只吃本地路径，不读 gist URL。

## 统一命令

```bash
python3 ~/work/hermes-agent/packages/ai-berkshire/tools/report_audit.py extract \
  --report <临时报告文件路径>

python3 ~/work/hermes-agent/packages/ai-berkshire/tools/report_audit.py verdict \
  --results '<填好的JSON>' \
  --report <临时报告文件路径>
```
