# connecttoGithub
ssh-keygen -t ed25519 -C "mahnoor@gmail.com"

enter 

enter

eval "$(ssh-agent -s)"

ubuntu@ip-172-31-1-201:~/django_bm$ ~/.ssh/config

-bash: /home/ubuntu/.ssh/config: No such file or directory

ubuntu@ip-172-31-1-201:~/django_bm$ touch ~/.ssh/config

ubuntu@ip-172-31-1-201:~/django_bm$ vim ~/.ssh/config


Host *

    AddKeysToAgent yes
    
    IdentityFile ~/.ssh/id_ed25519


ubuntu@ip-172-31-1-201:~/django_bm$ ssh-add ~/.ssh/id_ed25519

 cat ~/.ssh/id_ed25519.pub
paste its content in github ssh

# testing:
ssh -T git@github.com

# to remove:
rm -r ~/.ssh/config

rm -r home/<user>/.ssh/id_ed25519
