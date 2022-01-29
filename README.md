# Chinese_Handwriting_Recognition
HEBUT大四上学期校内实习项目 基于OpenCV和CNN的汉字手写识别系统

[![forthebadge](data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMzkuNjgiIGhlaWdodD0iMzUiIHZpZXdCb3g9IjAgMCAyMzkuNjggMzUiPjxyZWN0IGNsYXNzPSJzdmdfX3JlY3QiIHg9IjAiIHk9IjAiIHdpZHRoPSI5Ny43MTAwMDAwMDAwMDAwMSIgaGVpZ2h0PSIzNSIgZmlsbD0iIzMxQzRGMyIvPjxyZWN0IGNsYXNzPSJzdmdfX3JlY3QiIHg9Ijk1LjcxMDAwMDAwMDAwMDAxIiB5PSIwIiB3aWR0aD0iMTQzLjk3IiBoZWlnaHQ9IjM1IiBmaWxsPSIjMzg5QUQ1Ii8+PHBhdGggY2xhc3M9InN2Z19fdGV4dCIgZD0iTTE3LjMzIDIyTDE0LjIyIDIyTDE0LjIyIDEzLjQ3TDE3LjE0IDEzLjQ3UTE4LjU5IDEzLjQ3IDE5LjM0IDE0LjA1UTIwLjEwIDE0LjYzIDIwLjEwIDE1Ljc4TDIwLjEwIDE1Ljc4UTIwLjEwIDE2LjM2IDE5Ljc4IDE2LjgzUTE5LjQ3IDE3LjMwIDE4Ljg2IDE3LjU2TDE4Ljg2IDE3LjU2UTE5LjU1IDE3Ljc1IDE5LjkzIDE4LjI2UTIwLjMxIDE4Ljc4IDIwLjMxIDE5LjUxTDIwLjMxIDE5LjUxUTIwLjMxIDIwLjcxIDE5LjUzIDIxLjM2UTE4Ljc2IDIyIDE3LjMzIDIyTDE3LjMzIDIyWk0xNS43MCAxOC4xNUwxNS43MCAyMC44MkwxNy4zNSAyMC44MlExOC4wNCAyMC44MiAxOC40NCAyMC40N1ExOC44MyAyMC4xMyAxOC44MyAxOS41MUwxOC44MyAxOS41MVExOC44MyAxOC4xOCAxNy40NyAxOC4xNUwxNy40NyAxOC4xNUwxNS43MCAxOC4xNVpNMTUuNzAgMTQuNjZMMTUuNzAgMTcuMDZMMTcuMTUgMTcuMDZRMTcuODQgMTcuMDYgMTguMjMgMTYuNzVRMTguNjIgMTYuNDMgMTguNjIgMTUuODZMMTguNjIgMTUuODZRMTguNjIgMTUuMjMgMTguMjYgMTQuOTVRMTcuOTAgMTQuNjYgMTcuMTQgMTQuNjZMMTcuMTQgMTQuNjZMMTUuNzAgMTQuNjZaTTI0LjY0IDE5LjE2TDI0LjY0IDE5LjE2TDI0LjY0IDEzLjQ3TDI2LjEyIDEzLjQ3TDI2LjEyIDE5LjE4UTI2LjEyIDIwLjAzIDI2LjU1IDIwLjQ4UTI2Ljk4IDIwLjkzIDI3LjgzIDIwLjkzTDI3LjgzIDIwLjkzUTI5LjU0IDIwLjkzIDI5LjU0IDE5LjEzTDI5LjU0IDE5LjEzTDI5LjU0IDEzLjQ3TDMxLjAyIDEzLjQ3TDMxLjAyIDE5LjE3UTMxLjAyIDIwLjUzIDMwLjE1IDIxLjMyUTI5LjI4IDIyLjEyIDI3LjgzIDIyLjEyTDI3LjgzIDIyLjEyUTI2LjM2IDIyLjEyIDI1LjUwIDIxLjMzUTI0LjY0IDIwLjU1IDI0LjY0IDE5LjE2Wk0zNy4xNSAyMkwzNS42NyAyMkwzNS42NyAxMy40N0wzNy4xNSAxMy40N0wzNy4xNSAyMlpNNDcuMzIgMjJMNDEuOTYgMjJMNDEuOTYgMTMuNDdMNDMuNDQgMTMuNDdMNDMuNDQgMjAuODJMNDcuMzIgMjAuODJMNDcuMzIgMjJaTTUzLjEyIDE0LjY2TDUwLjQ5IDE0LjY2TDUwLjQ5IDEzLjQ3TDU3LjI1IDEzLjQ3TDU3LjI1IDE0LjY2TDU0LjU5IDE0LjY2TDU0LjU5IDIyTDUzLjEyIDIyTDUzLjEyIDE0LjY2Wk03MC4xMCAyMkw2Ni45OSAyMkw2Ni45OSAxMy40N0w2OS45MSAxMy40N1E3MS4zNiAxMy40NyA3Mi4xMSAxNC4wNVE3Mi44NyAxNC42MyA3Mi44NyAxNS43OEw3Mi44NyAxNS43OFE3Mi44NyAxNi4zNiA3Mi41NSAxNi44M1E3Mi4yNCAxNy4zMCA3MS42MyAxNy41Nkw3MS42MyAxNy41NlE3Mi4zMiAxNy43NSA3Mi43MCAxOC4yNlE3My4wNyAxOC43OCA3My4wNyAxOS41MUw3My4wNyAxOS41MVE3My4wNyAyMC43MSA3Mi4zMCAyMS4zNlE3MS41MyAyMiA3MC4xMCAyMkw3MC4xMCAyMlpNNjguNDcgMTguMTVMNjguNDcgMjAuODJMNzAuMTIgMjAuODJRNzAuODEgMjAuODIgNzEuMjEgMjAuNDdRNzEuNjAgMjAuMTMgNzEuNjAgMTkuNTFMNzEuNjAgMTkuNTFRNzEuNjAgMTguMTggNzAuMjQgMTguMTVMNzAuMjQgMTguMTVMNjguNDcgMTguMTVaTTY4LjQ3IDE0LjY2TDY4LjQ3IDE3LjA2TDY5LjkyIDE3LjA2UTcwLjYxIDE3LjA2IDcxLjAwIDE2Ljc1UTcxLjM5IDE2LjQzIDcxLjM5IDE1Ljg2TDcxLjM5IDE1Ljg2UTcxLjM5IDE1LjIzIDcxLjAzIDE0Ljk1UTcwLjY3IDE0LjY2IDY5LjkxIDE0LjY2TDY5LjkxIDE0LjY2TDY4LjQ3IDE0LjY2Wk03OS41OCAxOC44Nkw3Ni43MiAxMy40N0w3OC4zNyAxMy40N0w4MC4zMyAxNy41MUw4Mi4yOSAxMy40N0w4My45MyAxMy40N0w4MS4wNyAxOC44Nkw4MS4wNyAyMkw3OS41OCAyMkw3OS41OCAxOC44NloiIGZpbGw9IiNGRkZGRkYiLz48cGF0aCBjbGFzcz0ic3ZnX190ZXh0IiBkPSJNMTA4LjgyIDIwLjkzTDEwOC44MiAyMC45M0wxMTAuMTEgMTkuNDBRMTEwLjc4IDIwLjI3IDExMS41NiAyMC4yN0wxMTEuNTYgMjAuMjdRMTExLjU2IDIwLjI3IDExMS41NyAyMC4yN0wxMTEuNTcgMjAuMjdRMTEyLjA4IDIwLjI3IDExMi4zNSAxOS45NlExMTIuNjIgMTkuNjUgMTEyLjYyIDE5LjA1TDExMi42MiAxOS4wNUwxMTIuNjIgMTUuNDRMMTA5LjcyIDE1LjQ0TDEwOS43MiAxMy42MEwxMTQuOTggMTMuNjBMMTE0Ljk4IDE4LjkxUTExNC45OCAyMC41NCAxMTQuMTUgMjEuMzZRMTEzLjMzIDIyLjE3IDExMS43NCAyMi4xN0wxMTEuNzQgMjIuMTdRMTEwLjgxIDIyLjE3IDExMC4wNiAyMS44NVExMDkuMzAgMjEuNTMgMTA4LjgyIDIwLjkzWk0xMjYuODEgMjJMMTIwLjA2IDIyTDEyMC4wNiAxMy42MEwxMjYuNjYgMTMuNjBMMTI2LjY2IDE1LjQ0TDEyMi40MiAxNS40NEwxMjIuNDIgMTYuODVMMTI2LjE1IDE2Ljg1TDEyNi4xNSAxOC42M0wxMjIuNDIgMTguNjNMMTIyLjQyIDIwLjE3TDEyNi44MSAyMC4xN0wxMjYuODEgMjJaTTEzMy45OSAyMkwxMzEuNjEgMjJMMTMxLjYxIDEzLjYwTDEzNS40NiAxMy42MFExMzYuNjAgMTMuNjAgMTM3LjQ0IDEzLjk4UTEzOC4yNyAxNC4zNSAxMzguNzMgMTUuMDZRMTM5LjE5IDE1Ljc2IDEzOS4xOSAxNi43MUwxMzkuMTkgMTYuNzFRMTM5LjE5IDE3LjYyIDEzOC43NiAxOC4zMFExMzguMzMgMTguOTggMTM3LjU0IDE5LjM2TDEzNy41NCAxOS4zNkwxMzkuMzUgMjJMMTM2LjgxIDIyTDEzNS4yOSAxOS43N0wxMzMuOTkgMTkuNzdMMTMzLjk5IDIyWk0xMzMuOTkgMTUuNDdMMTMzLjk5IDE3LjkzTDEzNS4zMSAxNy45M1ExMzYuMDQgMTcuOTMgMTM2LjQxIDE3LjYxUTEzNi43OSAxNy4yOSAxMzYuNzkgMTYuNzFMMTM2Ljc5IDE2LjcxUTEzNi43OSAxNi4xMiAxMzYuNDEgMTUuNzlRMTM2LjA0IDE1LjQ3IDEzNS4zMSAxNS40N0wxMzUuMzEgMTUuNDdMMTMzLjk5IDE1LjQ3Wk0xNDYuMzUgMjJMMTQzLjk4IDIyTDE0My45OCAxMy42MEwxNDcuODIgMTMuNjBRMTQ4Ljk2IDEzLjYwIDE0OS44MCAxMy45OFExNTAuNjQgMTQuMzUgMTUxLjEwIDE1LjA2UTE1MS41NSAxNS43NiAxNTEuNTUgMTYuNzFMMTUxLjU1IDE2LjcxUTE1MS41NSAxNy42MiAxNTEuMTIgMTguMzBRMTUwLjcwIDE4Ljk4IDE0OS45MSAxOS4zNkwxNDkuOTEgMTkuMzZMMTUxLjcyIDIyTDE0OS4xNyAyMkwxNDcuNjUgMTkuNzdMMTQ2LjM1IDE5Ljc3TDE0Ni4zNSAyMlpNMTQ2LjM1IDE1LjQ3TDE0Ni4zNSAxNy45M0wxNDcuNjcgMTcuOTNRMTQ4LjQxIDE3LjkzIDE0OC43OCAxNy42MVExNDkuMTUgMTcuMjkgMTQ5LjE1IDE2LjcxTDE0OS4xNSAxNi43MVExNDkuMTUgMTYuMTIgMTQ4Ljc4IDE1Ljc5UTE0OC40MSAxNS40NyAxNDcuNjcgMTUuNDdMMTQ3LjY3IDE1LjQ3TDE0Ni4zNSAxNS40N1pNMTU4LjQ3IDE4Ljk1TDE1NS4yNiAxMy42MEwxNTcuNzcgMTMuNjBMMTU5Ljc2IDE2Ljk0TDE2MS43NSAxMy42MEwxNjQuMDYgMTMuNjBMMTYwLjg0IDE4Ljk5TDE2MC44NCAyMkwxNTguNDcgMjJMMTU4LjQ3IDE4Ljk1Wk0xNzcuMTkgMjJMMTc0LjQ3IDEzLjYwTDE3Ni45MiAxMy42MEwxNzguNjAgMTguOTZMMTgwLjM4IDEzLjYwTDE4Mi41NyAxMy42MEwxODQuMjYgMTkuMDFMMTg2LjAyIDEzLjYwTDE4OC4yOSAxMy42MEwxODUuNTcgMjJMMTgzLjAyIDIyTDE4MS40MiAxNi44OUwxNzkuNzQgMjJMMTc3LjE5IDIyWk0xOTQuMjIgMjJMMTkxLjc5IDIyTDE5NS41MCAxMy42MEwxOTcuODUgMTMuNjBMMjAxLjU2IDIyTDE5OS4xMCAyMkwxOTguNDMgMjAuMzdMMTk0Ljg4IDIwLjM3TDE5NC4yMiAyMlpNMTk2LjY2IDE1LjkzTDE5NS41NyAxOC42MUwxOTcuNzQgMTguNjFMMTk2LjY2IDE1LjkzWk0yMDguMDUgMjJMMjA1LjcyIDIyTDIwNS43MiAxMy42MEwyMDcuNjcgMTMuNjBMMjExLjM4IDE4LjA3TDIxMS4zOCAxMy42MEwyMTMuNzEgMTMuNjBMMjEzLjcxIDIyTDIxMS43NiAyMkwyMDguMDUgMTcuNTJMMjA4LjA1IDIyWk0yMTguNDQgMTcuODBMMjE4LjQ0IDE3LjgwUTIxOC40NCAxNi41NCAyMTkuMDQgMTUuNTRRMjE5LjY0IDE0LjU1IDIyMC43MSAxMy45OVEyMjEuNzggMTMuNDMgMjIzLjEyIDEzLjQzTDIyMy4xMiAxMy40M1EyMjQuMzAgMTMuNDMgMjI1LjIzIDEzLjgzUTIyNi4xNyAxNC4yMiAyMjYuNzkgMTQuOTdMMjI2Ljc5IDE0Ljk3TDIyNS4yOCAxNi4zM1EyMjQuNDQgMTUuNDAgMjIzLjI2IDE1LjQwTDIyMy4yNiAxNS40MFEyMjMuMjUgMTUuNDAgMjIzLjI0IDE1LjQwTDIyMy4yNCAxNS40MFEyMjIuMTYgMTUuNDAgMjIxLjUwIDE2LjA2UTIyMC44NCAxNi43MSAyMjAuODQgMTcuODBMMjIwLjg0IDE3LjgwUTIyMC44NCAxOC41MCAyMjEuMTQgMTkuMDRRMjIxLjQ0IDE5LjU5IDIyMS45OCAxOS44OVEyMjIuNTIgMjAuMjAgMjIzLjIyIDIwLjIwTDIyMy4yMiAyMC4yMFEyMjMuOTAgMjAuMjAgMjI0LjUwIDE5LjkzTDIyNC41MCAxOS45M0wyMjQuNTAgMTcuNjJMMjI2LjYwIDE3LjYyTDIyNi42MCAyMS4xMFEyMjUuODggMjEuNjEgMjI0Ljk0IDIxLjg5UTIyNC4wMSAyMi4xNyAyMjMuMDcgMjIuMTdMMjIzLjA3IDIyLjE3UTIyMS43NSAyMi4xNyAyMjAuNzAgMjEuNjFRMjE5LjY0IDIxLjA1IDIxOS4wNCAyMC4wNVEyMTguNDQgMTkuMDYgMjE4LjQ0IDE3LjgwWiIgZmlsbD0iI0ZGRkZGRiIgeD0iMTA4LjcxMDAwMDAwMDAwMDAxIi8+PC9zdmc+)](https://wangjiayi.cool)

[![forthebadge](https://forthebadge.com/images/badges/fuck-it-ship-it.svg)](https://forthebadge.com)

## 项目说明（先占个地 代码懒得上传）

1. HWDB1.0数据集处理.py
2. MobileNet V2.0网络结构.py
3. 模型训练.py
4. 基于水平垂直投影分割的手写检测.py
5. 服务端.py
6. 用户端网页.html .css
7. 基于Canvas的网页手写输入.js 

## 未来计划（还不知道什么时候再研究）

- [ ] 扩大训练集，支持全部常用汉字
- [ ] 训练Detect模型，替换掉现有的分割算法
- [ ] 优化网络结构
