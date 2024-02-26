# EXERCISE 1.1: GETTING STARTED
Since we already did "Hello, World!" in the material let's do something else.
Start 3 containers from an image that does not automatically exit (such as nginx) in detached mode.
Stop two of the containers and leave one container running.
Submit the output for docker ps -a which shows 2 stopped containers and one running.

- NRangel@NRangel-Mac Learning % docker ps -a
    - CONTAINER ID   IMAGE                                     COMMAND                  CREATED         STATUS                        PORTS     NAMES
    - 2b9e04272f7c   nginx                                     "/docker-entrypoint.…"   3 minutes ago   Up 23 seconds                 80/tcp    youthful_moser
    - 25d556ff3f43   nginx                                     "/docker-entrypoint.…"   5 minutes ago   Exited (127) 19 seconds ago             vigorous_rubin
    - d5095ccbe2bc   nginx                                     "/docker-entrypoint.…"   5 minutes ago   Exited (127) 12 seconds ago             sleepy_yonath

# EXERCISE 1.2: CLEANUP
We have containers and an image that are no longer in use and are taking up space. Running docker ps -as and docker images will confirm this.
Clean the Docker daemon by removing all images and containers.
Submit the output for docker ps -a and docker images

- NRangel@NRangel-Mac Learning % docker container rm youthful_moser
  youthful_moser
-  NRangel@NRangel-Mac Learning % docker container rm vigorous_rubin
  vigorous_rubin
-  NRangel@NRangel-Mac Learning % docker container rm sleepy_yonath
  sleepy_yonath
-  NRangel@NRangel-Mac Learning % docker ps -a

- NRangel@NRangel-Mac Learning % docker image rm nginx
Untagged: nginx:latest
Untagged: nginx@sha256:c26ae7472d624ba1fafd296e73cecc4f93f853088e6a9c13c0d52f6ca5865107
Deleted: sha256:760b7cbba31e196288effd2af6924c42637ac5e0d67db4de6309f24518844676
Deleted: sha256:957ebc1bdcc4523205c62dececc2e4176cc3fec0d163daaf46e438010c343c8e
Deleted: sha256:87ce81aab221a837e6ba352143754d92aa8957170132d9e9a1b0d1eb6b9b8250
Deleted: sha256:497653d7af24e3edbf1cb9d2ac2718e7941acfa9957c7a9a735f54b29cc2b446
Deleted: sha256:0af4f4db5d95ae5e8cb002a587a5a70a48420d8caf4f560f6c83bebb53424946
Deleted: sha256:4d0cb5956e33f68639568804299b395719e3e2f50403cffe8105d83940cea87d
Deleted: sha256:eb4f25154f24b12f06797c598d8473d8ad4d6dd56fc0ad21dcf49e3dcc72f17a
- NRangel@NRangel-Mac Learning % docker image rm mongo
Untagged: mongo:latest
Untagged: mongo@sha256:5a54d0323fe207d15dc48773a7b9e7e519f83ad94a19c2ddac201d7aae109eb1
Deleted: sha256:c313d60605ed3771fab3e536d9029ef80c3835100810b4a9391fc3dfc55d0894
Deleted: sha256:b95a14c610fdbb623dd8105d38160e9a9864bbdf19131ec557bfb93864cf6716
Deleted: sha256:1488cf650f9a3046f67f646fcbd5ce561d137beb2b5bd5be9afc78a8b7e9d372
Deleted: sha256:536b2705a01b29d94baf3d2406bb1dc41f9ca27be811680d310a71d556ab612c
Deleted: sha256:7b42d5beba067cf7fe22910e8af29ad4558b8d902c7a1aa873e75704b181ef45
Deleted: sha256:0c4bf7b24678fbafa640f4e12fddc75a7a254726d37877fc0336914d43b2a305
Deleted: sha256:73f27f89a60248da68444bef81b9d4d5cc01ab5eb5b823ce53379eeeba9e80c8
Deleted: sha256:3fd27f7f9f0fa9597ed99714bb8f2fa3a423e8ce43ee91b6069bdee145f66032
Deleted: sha256:98d1994bf6c1db82b81822e3b2f8fdb6933c44fcd9487787c41ee907368022e2
- NRangel@NRangel-Mac Learning % docker image rm postgres
Untagged: postgres:latest
Untagged: postgres@sha256:0e564daae78c2eea56ba57c64711bb9c408a512ce73cf81f9c78623354dd6976
Deleted: sha256:75793281f730b3949981b39076f1cd71e7cbc66be096c39b34f8495950bb9ef9
Deleted: sha256:b01df75a05d637ca216f6ae904e5acb220d0c3b4eca196ec6a970415bc1d1e39
Deleted: sha256:f73b62bd6ee48093ac64c39aac40f61e4c1a93710a495ba745da8c25dc2cc93c
Deleted: sha256:43a03a6a389b8f9a99365be057609d73a4cb8a241012bc3a066ce02cb60eef21
Deleted: sha256:39008c22c316c3b16661df56fce7a6cd585302467fc1d49b954514b1c20b15e4
Deleted: sha256:aecf019b5d438331cd713707945880590bcd2d6f6a72a44ba5e42c796f507bf7
Deleted: sha256:053e98c9caf4eaa5b7749daad0e6d86a3d510efc31b292d607f6fa1f129fc033
Deleted: sha256:5bbad87815f755a77a43f37fcb2399de5f801e86adbe18eb097d7e88bd1be097
Deleted: sha256:85cedb4f9cc88b77a40fd360de195d02a70e05db1d366fd6df588d23e6d3d9f4
Deleted: sha256:a1edf934d4983e57f46d5b7b2b0402cf0fef6031585f3492e865bf7529d760e1
Deleted: sha256:075c95c2cdd858625ce6dc2652d4aa9afe0e4d9361649600960d5f04988654cc
Deleted: sha256:9badb49fbad5f3afa97dbe5c7059682173d5b19b112ee5054cd778070a09b96f
Deleted: sha256:658a959dc791c42c00f7e5140643943694faae1989655ca7e1118cc9ebe81848
Deleted: sha256:39fe0cdc91c32759fb5e26fa7dab2b448e2b479520ee8d20971e610f8fd45d6d
Deleted: sha256:644fed2a38987e9c2e23a98fbd38f898ab6ab64c8473b9123bdd970bb77c1437
-  NRangel@NRangel-Mac Learning % docker ps -a

- Unable to show clear image and container log due to other projects