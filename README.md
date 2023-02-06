# [Style Transfer Description](https://gitee.com/mindspore/models/blob/r1.6/research/cv/ArbitraryStyleTransfer/README.md#contents)

This is the Implementation of the Mindspore code of paper [**Exploring the structure of a real-time, arbitrary neural artistic stylization network.**](https://gitee.com/link?target=https%3A%2F%2Farxiv.org%2Fabs%2F1705.06830)

Authors: [Golnaz Ghiasi](https://gitee.com/link?target=https%3A%2F%2Farxiv.org%2Fsearch%2Fcs%3Fsearchtype%3Dauthor%26query%3DGhiasi%252C%2BG), [Honglak Lee](https://gitee.com/link?target=https%3A%2F%2Farxiv.org%2Fsearch%2Fcs%3Fsearchtype%3Dauthor%26query%3DLee%252C%2BH), [Manjunath Kudlur](https://gitee.com/link?target=https%3A%2F%2Farxiv.org%2Fsearch%2Fcs%3Fsearchtype%3Dauthor%26query%3DKudlur%252C%2BM), [Vincent Dumoulin](https://gitee.com/link?target=https%3A%2F%2Farxiv.org%2Fsearch%2Fcs%3Fsearchtype%3Dauthor%26query%3DDumoulin%252C%2BV), [Jonathon Shlens](https://gitee.com/link?target=https%3A%2F%2Farxiv.org%2Fsearch%2Fcs%3Fsearchtype%3Dauthor%26query%3DShlens%252C%2BJ)

In this paper, we present a method which combines the flexibility of the neural algorithm of artistic style with the speed of fast style transfer networks to allow real-time stylization using any content/style image pair. We build upon recent work leveraging conditional instance normalization for multi-style transfer networks by learning to predict the conditional instance normalization parameters directly from a style image. The model is successfully trained on a corpus of roughly 80,000 paintings and is able to generalize to paintings previously unobserved. We demonstrate that the learned embedding space is smooth and contains a rich structure and organizes semantic information associated with paintings in an entirely unsupervised manner.

# [Model Architecture](https://gitee.com/mindspore/models/blob/r1.6/research/cv/ArbitraryStyleTransfer/README.md#contents)

![img](https://gitee.com/mindspore/models/raw/r1.6/research/cv/ArbitraryStyleTransfer/assets/network.png)

The style prediction network P predicts an embedding vector S from an input style image, which supplies a set of normalization constants for the style transfer network. The style transfer network transforms the photograph into a stylized representation. The content and style losses are derived from the distance in representational space of the VGG image classification network. The style transfer network largely follows and the style prediction network largely follows the Inception-v3 architecture.

[RepoLink](https://gitee.com/mindspore/models/tree/r1.6/research/cv/ArbitraryStyleTransfer)