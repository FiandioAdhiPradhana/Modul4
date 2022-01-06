# # **Modul 4 Practicum Report**

### By : Fairuzrizqi Nugraharsanto  &  Budhi Priambodo

* First, make 2 copies of containers, and then start

![Screenshot (323)](https://user-images.githubusercontent.com/92350603/148335067-b8f6db73-4f00-494b-9f5e-e45c0b3ee66e.png)

![Screenshot (324)](https://user-images.githubusercontent.com/92350603/148335063-f84e4651-242b-4a69-b0ee-32bab0cc0649.png)


* Next, open ubuntu_php7.4_2 and change the IP address to 10.0.3.111/24. Do the same thing on ubuntu_php7.4_3, change the IP address to 10.0.3.121

![Screenshot (325)](https://user-images.githubusercontent.com/92350603/148335112-d51ac500-d1ad-4855-b9bd-b5d3e4ce38c4.png)


* Go to lxc_php7_2.dev and change the server name

![Screenshot (326)](https://user-images.githubusercontent.com/92350603/148335194-27de4b59-1893-477d-924b-90e551b8c3e0.png)
![Jepretan Layar 2022-01-06 pada 4 41 05 PM](https://user-images.githubusercontent.com/93086665/148404304-e5fe530f-7add-4b4c-8dfa-bdd126a83f27.png)

* Restart nginx and curl it. 
* Next step is ubuntu_php7.4_3 (IP 10.0.3.121), debian_php5.6_2 (IP 10.0.3.112), debian_php5.6_3 (IP 10.0.3.122) the same as ubuntu_php7.4_2.
* Add name server /etc/hosts (on VM)

![Jepretan Layar 2022-01-06 pada 4 43 20 PM](https://user-images.githubusercontent.com/93086665/148404524-427b1fde-6aac-426f-a10b-516208e31210.png)


* Run the jmeter, and change the number of threads

![Jepretan Layar 2022-01-06 pada 5 08 11 PM](https://user-images.githubusercontent.com/93086665/148404875-defc7347-bae7-480b-b262-d382b10325b9.png)
![Jepretan Layar 2022-01-06 pada 5 08 40 PM](https://user-images.githubusercontent.com/93086665/148404892-3131a076-9168-4996-84f9-89b63c43e09e.png)
![(1)Jepretan Layar 2022-01-06 pada 5 02 44 PM](https://user-images.githubusercontent.com/93086665/148404903-c96f4153-fd0e-4795-9fe3-b98f6d1d86e0.png)
![Jepretan Layar 2022-01-06 pada 5 03 15 PM](https://user-images.githubusercontent.com/93086665/148404911-6ff5ad08-1fef-47b8-abe5-90a009a1636b.png)
![Jepretan Layar 2022-01-06 pada 5 03 52 PM](https://user-images.githubusercontent.com/93086665/148404921-3e1fa238-0c7d-4c2a-ac6a-b0e84d3b0026.png)
![Jepretan Layar 2022-01-06 pada 5 04 26 PM](https://user-images.githubusercontent.com/93086665/148404933-bebbd4c6-44a5-437c-be8d-0ce4fe7a6cd7.png)
![Jepretan Layar 2022-01-06 pada 5 05 35 PM](https://user-images.githubusercontent.com/93086665/148404943-b3c1103f-d7d3-4d56-a940-462283321a33.png)
![Jepretan Layar 2022-01-06 pada 5 06 16 PM](https://user-images.githubusercontent.com/93086665/148404945-5eb92630-e530-4bba-922f-0616e8f744b6.png)
![Jepretan Layar 2022-01-06 pada 5 06 47 PM](https://user-images.githubusercontent.com/93086665/148404952-0474190a-98dc-4484-b58d-1d8bf012a93d.png)
![Jepretan Layar 2022-01-06 pada 5 07 03 PM](https://user-images.githubusercontent.com/93086665/148404964-4f97d4c3-694c-4b41-849b-e6651b5260a1.png)
![Jepretan Layar 2022-01-06 pada 5 07 29 PM](https://user-images.githubusercontent.com/93086665/148404970-61826dfd-588c-4736-849b-4d8e77fce9aa.png)
![Jepretan Layar 2022-01-06 pada 5 07 56 PM](https://user-images.githubusercontent.com/93086665/148404979-fa04bcc7-0c12-4509-92a0-986bbbb82364.png)

Go back to the VM and write the script as below to add upstream landing, php5,and php7


```markdown
nano /etc/nginx/sites-available/vm.local
```
to add upstream landing, php5, and php7
  
![Jepretan Layar 2022-01-06 pada 5 18 21 PM](https://user-images.githubusercontent.com/93086665/148405189-12237d26-aef7-4af9-8ac9-b4db5278dd0d.png)

change the proxy_pass

![Jepretan Layar 2022-01-06 pada 5 19 31 PM](https://user-images.githubusercontent.com/93086665/148405358-e5bbd45f-4b97-4e8e-9164-4f0058e8d9ce.png)

  
Then we go back to the jmeter 
  
* 50

![Jepretan Layar 2022-01-06 pada 5 20 45 PM](https://user-images.githubusercontent.com/93086665/148405480-a54db4bd-efc6-4fc8-9b27-2ce9e4c3c4a3.png)
![Jepretan Layar 2022-01-06 pada 5 21 03 PM](https://user-images.githubusercontent.com/93086665/148405508-1df861ca-f6ca-4db2-878c-6fc726ac3b4e.png)
![Jepretan Layar 2022-01-06 pada 5 21 18 PM](https://user-images.githubusercontent.com/93086665/148405523-3bd6057d-cf0a-4dfd-97dd-3303e5c3483c.png)
![Jepretan Layar 2022-01-06 pada 5 21 36 PM](https://user-images.githubusercontent.com/93086665/148405535-85ac4112-c1b9-470c-8b10-d81dbd950f59.png)


* 100
![Jepretan Layar 2022-01-06 pada 5 22 24 PM](https://user-images.githubusercontent.com/93086665/148405640-76684c35-2a6f-4191-aec2-6bb8568426b9.png)
![Jepretan Layar 2022-01-06 pada 5 22 37 PM](https://user-images.githubusercontent.com/93086665/148405664-02e58e14-28bb-431f-9c4b-8364b2d5bb08.png)
![Jepretan Layar 2022-01-06 pada 5 22 52 PM](https://user-images.githubusercontent.com/93086665/148405684-29beb0ed-96c4-43f3-a635-16e7ee046f81.png)
![Jepretan Layar 2022-01-06 pada 5 21 52 PM](https://user-images.githubusercontent.com/93086665/148405699-cc513ef2-590e-4261-9c5c-975fa728c086.png)

* 150
![Jepretan Layar 2022-01-06 pada 5 23 03 PM](https://user-images.githubusercontent.com/93086665/148405812-70cbf491-27bf-4fb7-8c40-dc511e692930.png)
![Jepretan Layar 2022-01-06 pada 5 24 24 PM](https://user-images.githubusercontent.com/93086665/148405850-517d3dee-037b-496f-9e61-92e45799ee19.png)
![Jepretan Layar 2022-01-06 pada 5 24 34 PM](https://user-images.githubusercontent.com/93086665/148405874-3e20e8b0-1d30-480c-ae74-8369db0cc151.png)
![Jepretan Layar 2022-01-06 pada 5 24 45 PM](https://user-images.githubusercontent.com/93086665/148405885-5f3ddce5-8827-4487-95ba-6e05ef17f175.png)


### Analysis

Below is the results from when we use load balancer and not using the load balancer

 - When there is 50 users that access our web, if we don't use load balancer the average time of user accessing our web is
   - landing : 1115 ms / 1.1 s
   - blog : 1555 ms / 1.5 s
   - app : 4 ms / 0.004 s
- When we use load balancer, then
   - landing : 37 ms / 0.037 s
   - blog : 27 ms / 0.027 s
   - app : 21 ms / 0.021 s

Here we can know that the average time of user accessing our web is faster then if we don't use load balancer. For the throughput or the amount of user accessing our web is
- When there is 50 users that access our web, if we don't use load balancer the amount of user accessing our web is

  - landing : 36 user / second
  - blog :  20 user / second
  - app : 41 user / second

- When we use load balancer, then

  - landing : 427 user / second
  - blog :  439 user / second
  - app : 446 user / second

The conclusion is, if we use load balancer, then the time is faster and the amount of users that accessing our web is much more then when we don't use load balancer.

*Thank you* 
