# 常见问题
root@Ubuntu1604-10:~/tape-0.1.0# ./stupid config.yaml 10
panic: Received nil message, but expect a valid block instead. You could look into your peer logs for more info

goroutine 467 [running]:
github.com/guoger/stupid/pkg/infra.(*Observer).Start(0xc00037f180, 0xa, 0xbfedd866067950a6, 0x4d5d71d, 0xf40200)
        /root/tape-0.1.0/pkg/infra/observer.go:55 +0x3b2
created by main.main
        /root/tape-0.1.0/cmd/stupid/main.go:60 +0x6cc
        
tape0.1.0测试新华三gaea平台的链码遇到peer节点报错
docker日志如下，该怎么解决？

peer docker logs
2020-12-14 03:47:35.320 UTC [core.comm] ServerHandshake -> ERRO 1df TLS handshake failed with error EOF server=PeerServer remoteaddress=72.1.18.1:35556
2020-12-14 03:49:35.476 UTC [core.comm] ServerHandshake -> ERRO 1e0 TLS handshake failed with error EOF server=PeerServer remoteaddress=72.1.18.1:37274
2020-12-14 03:49:53.560 UTC [core.comm] ServerHandshake -> ERRO 1e1 TLS handshake failed with error tls: client didn't provide a certificate server=ChaincodeServer remoteaddress=172.16.0.28:48194
2020-12-14 03:51:35.616 UTC [core.comm] ServerHandshake -> ERRO 1e2 TLS handshake failed with error EOF server=PeerServer remoteaddress=72.1.18.1:39108
2020-12-14 03:53:35.756 UTC [core.comm] ServerHandshake -> ERRO 1e3 TLS handshake failed with error EOF server=PeerServer remoteaddress=72.1.18.1:41266

ca docker logs 
2020/12/14 04:24:58 [DEBUG] Cleaning up expired nonces for CA 'ca-org1'
2020/12/14 04:25:37 http: TLS handshake error from 72.1.18.1:46800: EOF
2020/12/14 04:27:38 http: TLS handshake error from 72.1.18.1:48434: EOF
2020/12/14 04:29:38 http: TLS handshake error from 72.1.18.1:50292: EOF
2020/12/14 04:31:38 http: TLS handshake error from 72.1.18.1:52014: EOF
2020/12/14 04:33:38 http: TLS handshake error from 72.1.18.1:53800: EOF
2020/12/14 04:35:38 http: TLS handshake error from 72.1.18.1:55634: EOF
