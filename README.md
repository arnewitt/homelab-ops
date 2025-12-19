# homelab-ops

## deployment

Create a `hosts.ini` in this project's root dir:

```bash
[my_server]
192.168.1.XX ansible_user=ubuntu
```

Set up your secrets in a `.env`file in the root dir:

```bash
OPENAI_API_KEY=sk-your-key-here
OPENAI_API_BASE_URL=your-url-here
WEBUI_SECRET_KEY=generate-a-long-random-string
```

Deploy: 

```bash
ansible-playbook -i hosts.ini homelab.yml --ask-become-pass
```