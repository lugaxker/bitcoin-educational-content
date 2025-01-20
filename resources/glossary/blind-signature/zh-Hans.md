---
term: 盲签

---
Chaum 的盲签名是一种数字签名形式，签名者不知道所签名的信息内容。然而，该签名随后可以与原始信息进行验证。这种技术由密码学家戴维-查姆于 1983 年开发。

例如，一家公司希望在不泄露合同等机密文件内容的情况下对其进行验证。该公司采用掩蔽程序，以可逆方式对原始文件进行加密转换。修改后的文件被发送给认证机构，认证机构在不知道基本内容的情况下进行盲签名。在收到经过掩蔽签名的文件后，公司会取消掩蔽签名。这样，一份原始文件就通过了权威机构的签名认证，而权威机构却从未见过原始内容。

因此，Chaum 的盲签名可以在不知道文件内容的情况下认证文件的真实性，从而确保用户数据的保密性和签名文件的完整性。

在比特币中，该协议被用于作为覆盖层的Chaumian银行系统（Cashu、Fedimint等），尤其是在Chaumian coinjoin协议中，以确保协调者无法将输入链接到输出。