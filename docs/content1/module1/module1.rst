認証、認可の流れ
===========================

本節では、BIG-IP APMとDuo Securityを連携させた場合の認証、認可の流れを示します。
詳細は、下図をご参照ください。

.. figure:: images/Duo-Auth-rev3.png
   :scale: 40%
   :align: center

   BIG-IPでForward Proxyを構成する際のオブジェクト

- **HTTP Explicit Profile**
  

  BIG-IPをクライアントから見た明示 (Explicit) プロキシとして設定する場合に利用するプロファイルです。


- **HTTP Transparent Profile**


  BIG-IPをクライアントから見た透過 (Transparent) プロキシとして設定する場合に利用するプロファイルです。


- **DNS Resolver**


  Forward Proxyとして動作するBIG-IPがクエリを行う、DNSサーバのアドレスを指定します。DNSサーバのレスポンスは、BIG-IP内にキャッシュされます。


- **Virtual Server**
  
   
  BIG-IPで、サービスを受け付けるリスナーとして動作します。Virtual Serverで指定したIPアドレスおよびポート番号を、クライアント端末のWebブラウザ等に設定します。
