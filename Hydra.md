## Hydra

[Hydra](https://github.com/vanhauser-thc/thc-hydra) is a brute-force tool that is use for password cracking created by [Van Hauser](https://github.com/vanhauser-thc) and [David Maciejak](https://ca.linkedin.com/in/davidmaciejak). It can perform rapid dictionary attacks against various network services. It works by taking a list of usernames and a list of passwords, then systematically trying each combination on the target system.


By default, Hydra is installed on [Kali Linux](https://www.kali.org/](https://www.kali.org/docs/introduction/what-is-kali-linux/)), an open-source debian based linux used for penetration testing and security auditing.

To use hydra, we can use the following commands:
```
hydra -L <LIST_OF_USERNAMES_FILE> -P <LIST_OF_PASSWORD_FILES> <ADDRESS_OF_THE_WEBSITE> -s <PORT> "/:username=^USER^&password=^PASS^:Invalid username or password" -o ~/hydra_output_files/hydra_results.txt
```
<br>

***Explaination:***

```-s``` refers to the port that we want to use.

```http-post-form``` Specifies that we're using HTTP POST method for form submission.

```/:username=^USER^&password=^PASS^:Invalid username or password``` refers to how to interact to the website.

```-o``` refers to which file we want to save result. In this case, it's the ```~/hydra_output_files/hydra_results.txt```.
<br>






