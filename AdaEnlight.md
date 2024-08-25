# AdaEnlight: Energy-aware Low-light Video Stream Enhancement on Mobile Devices
# 文章引用
Liu S, Li X, Zhou Z, et al. AdaEnlight: Energy-aware low-light video stream enhancement on mobile devices[J]. Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies, 2023, 6(4): 1-26.
# 问题背景
移动嵌入式设备在广泛配备摄像头后会在光线不佳的环境下拍摄大量低质量视频流。然而，采用现有视频增强策略在云端执行会由于视频编码损失导致不可避免的受限增强结果，而在本地进行增强，端侧设备则无法负担每秒20~30帧的增强数据量。
# 问题动机
由于视频流的视频帧之间存在着大量的时空相似性，因此无需对每帧视频帧执行完整的神经网络推理流程即可实现对视频帧的有效增强。
# 解决方法
- **可调低照度增强神经网络**：通过将神经网络与增强曲线相结合，低照度增强系统可以通过缓存之前视频帧的神经网络推理结果来减少当前帧的神经网络推理计算量，从而避免过多的能耗开销。
- **能耗自适应的自适应低照度增强**：通过对神经网络推理过程造成的能耗开销的离线分析与在线预测，低照度增强系统可以对增强质量与增强能耗开销进行权衡，从而在保证增强质量可控的范围内提供能耗友好的增强方案。
