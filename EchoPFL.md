# EchoPFL: Asynchronous Personalized Federated Learning on Mobile Devices with On-Demand Staleness Control
# 文章引用
Li X, Liu S, Zhou Z, et al. EchoPFL: Asynchronous Personalized Federated Learning on Mobile Devices with On-Demand Staleness Control[J]. Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies, 2024, 8(1): 1-22.
# 问题背景
具有丰富传感数据和本地计算能力的移动设备的兴起推动了这些设备上联邦学习（FL）的趋势。个性化联邦学习 (PFL) 的出现旨在为每个移动设备训练特定的深度模型，以解决数据异构性和不同的性能偏好问题。 然而，不同移动设备上训练时间差异很大，导致上传模型的延迟（当等待较慢的设备进行聚合时）或准确性下降（当聚合不等待而继续进行时）。 
# 问题动机
EchoPFL拟采用异步异步个性化联邦学习，即服务器在更新可用时立即聚合更新。 然而，现有的异步协议不适合 PFL，因为它们是为单个全局模型的联合训练而设计的。 当面临 PFL 中普遍存在的严重数据异质性时，它们会出现收敛缓慢和准确性下降的问题。 此外，它们通常会排除速度较慢的设备来进行过时控制，当这些设备拥有关键的个性化数据时，这会显着影响准确性。 因此，我们提出了EchoPFL，一种异步PFL的协调机制。 EchoPFL 的核心是包含所有移动设备的更新，无论其延迟如何。 为了应对慢速设备不可避免的陈旧问题，EchoPFL 重新修改了模型广播。 它利用无线网络中的不对称带宽和基于动态集群的 PFL，自适应的进行按需广播。
# 解决方法
- **数据感知动态客户端集群**：通过增量聚类和基于运行时反馈的聚类结构调整实现高效且准确的异步个性化聚类。方法基于预定义的聚类数量，首先根据权重参数间的L1距离进行快速聚类，其次根据运行时的聚类结果反馈采用特征之间的KL散度进行聚类调整。
- **集群内自适应模型广播**：在确定了集群后，EchoPFL会根据需要向集群内的客户端广播最新的聚合模型。由于集群内的数据分布相对均匀，对一定程度的过时具有更强的容忍度。此外，EchoPFL还能够预测最佳的广播频率，以在不影响准确性的情况下进一步降低下游通信成本。
# 系统实用性
方法一方面实现了异步条件下的个性化聚类，另一方面能够适应客户端动态的数据变化，进行按需聚类调整，从而维持在线高精度
