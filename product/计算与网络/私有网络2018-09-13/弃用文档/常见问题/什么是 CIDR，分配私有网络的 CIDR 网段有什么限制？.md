您好，CIDR 由用户指定的独立网络空间地址块，通过 IP 和掩码结合，实现对网络的整体划分。以 10.1.0.0/16 为例，斜杠左边为网络块的 IP，斜杠右边为网络块的掩码。通过设定掩码的大小，可以调整网络块的大小设定。网络块包括的IP数 = 2^(32-掩码)，因而 10.1.0.0/16 网络块最多包含 65536 个 IP 地址。

私有网络目前支持的网络空间掩码支持/28至/16之间，也就是您的私有网络空间最少包含 16、最大包含 65536 个 IP 地址。
目前私有网络支持三个网段的内网IP：10.a.0.0/8（a 属于 0~255）、172.b.0.0/16（b 属于 0 到 31）、192.168.0.0/16 。私有网络的 CIDR 可以为以上三个网段，或者是网段中的一部分。
子网的 CIDR 必须是所在私有网络组成的一部分。