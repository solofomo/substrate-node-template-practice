#课程5作业

✅  列出3个常用的宏、3个常用的存储数据结构
说明：使用 Substrate-node-template 的版本为 polkadot-v0.9.30（git clone -b polkadot-v0.9.30 --depth 1 https://github.com/substrate-developer-hub/substrate-node-template.git

常用的宏：
1. #[pallet::config]：用于定义 pallet 的配置 trait。定义常量和关联类型，例如运行时事件类型、费用等。这些关联类型和常量可以在运行时进行配置。
2. #[pallet::event]：用于定义 pallet 的事件。事件记录链上发生的特定操作，例如创建、撤销和转移存证。事件在调用执行后被触发，并包含有关操作的相关信息。
3. #[pallet::storage]：用于定义 pallet 的存储项。这些存储项用于存储链上的状态信息，例如账户余额、存证数据等。存储项定义不同的数据类型，如单值、映射或双键映射。
4. #[pallet::call]：用于定义 pallet 的调用。调用是链上用户可以执行的操作，例如创建存证、撤销存证等。它们通常接受参数并返回一个 DispatchResultWithPostInfo 类型的结果。
5. #[pallet::hooks]：用于定义 pallet 的钩子。钩子是在特定阶段自动执行的操作，例如在每个区块开始或结束时。可以实现钩子以执行清理、更新或其他自动操作。

常用的存储数据结构：
1. StorageValue<T>：用于存储单个值的简单存储结构。适用于保存全局单值，例如模块的配置参数。
2. StorageMap<Key, Value>：一个键值对映射的存储结构。用于存储具有唯一键和关联值的数据，例如跟踪账户余额。
3. StorageDoubleMap<Key1, Key2, Value>：一个双键值对映射的存储结构。用于存储具有两个唯一键和关联值的数据，例如跟踪两个账户之间的关系。
4. StorageNMap<NKeys, Value>：一个具有 N 个键的映射存储结构。用于存储具有 N 个唯一键和关联值的数据。它提供了更高的灵活性，可以用于实现复杂的数据关系。
5. StorageLinkedMap<Key, Value>：一个有序的键值对映射的存储结构。它允许按照插入顺序迭代键值对。适用于需要按照顺序访问元素的场景。

✅  实现存证模块的功能，包括：创建存证；撤销存证。
说明：使用 Substrate-node-template 的版本为 polkadot-v0.9.30（git clone -b polkadot-v0.9.30 --depth 1 https://github.com/substrate-developer-hub/substrate-node-template.git），提交的Github链接必须包含：⚠️代码运行的截图图片+⚠️全部代码
![image](https://user-images.githubusercontent.com/83760488/229035029-fbf3d5af-20aa-47b3-97c6-c8973680d254.png)
![image](https://user-images.githubusercontent.com/83760488/229035320-58399da7-17a0-4581-8662-3302199379c3.png)
![image](https://user-images.githubusercontent.com/83760488/229035412-1cdafe32-2677-4c97-a342-6e59cab7f2a1.png)
![image](https://user-images.githubusercontent.com/83760488/229035508-ed69b2a1-afd6-46d0-bde9-a2d290bb1e30.png)
![image](https://user-images.githubusercontent.com/83760488/229035592-a947ff20-8554-4e4c-a7a6-37309ff71f15.png)

✅ 为存证模块添加新的功能，转移存证，接收两个参数，一个是包含的哈希值，另一个是存证的接收账户地址。
说明：使用 Substrate-node-template 的版本为 polkadot-v0.9.30（git clone -b polkadot-v0.9.30 --depth 1 https://github.com/substrate-developer-hub/substrate-node-template.git），提交的Github链接必须包含：⚠️代码运行的截图图片+⚠️全部代码
alice把proof转给bob
transfer之前
![image](https://user-images.githubusercontent.com/83760488/229035939-48bd1faa-7134-4c7e-8e45-aa0c6d28de73.png)

调用transfer
![image](https://user-images.githubusercontent.com/83760488/229036115-daa7bc8b-02dd-4abb-a78b-63a951e16e7c.png)

transfer之后
![image](https://user-images.githubusercontent.com/83760488/229036205-14e9bcfb-51a7-48da-b156-13aea5d64106.png)
