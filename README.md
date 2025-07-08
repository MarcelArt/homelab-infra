# Infrastructure Devops Apta

## Setup 
Create htpasswd file with this command
```
htpasswd -Bc ./auth/htpasswd yourusername
```

- -B argument make a password encryption
- -c is for create new file
- yourusername is your username

Verify the file exist
```
cat ./auth/htpasswd
```
example output
```
yourusername:$2y$05$9sJp3LHp3pP3J3B.f2xxmu30pH1VX6kZQ2JAGCN3X78z0/N1.tL5e
```
to add more user just type
```
htpasswd -B ./auth/htpasswd anotheruser
```
we should omit the -c argument so the file is not created again

Last thing just run 
```
docker compose up -d
```