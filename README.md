# TVGen-Master
#### Terraform Virsh Generator
```
git clone https://github.com/mrofiq466/TVGen-Master.git
chmod +x TVGen-Master/tvgen
mv TVGen-Master/tvgen /usr/local/bin/
tvgen -h
```
#### File variable
Is most case-sensitive
```
[KEY]
PUBKEY1: ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDUT+QC2+vIH/zpGqi9cJMyaOlaVE7HrLrAjpsJtkVP6HTv+pBeM0ebU8qU5X7dLOm2/3Xiid8KCnpxJU12FjbpJq2z/w/thhqXNTqWlghhplb2d3vgh7AT5l7JPpeEkwVAQ73YElFK78CvYGiAN02QuGNw8/t0ICM7iatGqxamdbWMhsl5x1cJniU077ykxez8eJvee3NjuC4YSX/LBvWdPZ2O4pNtrALTFhGl8OeyjXlI1mq9J5KMCexlqufr2QDEGocHKbBRw0lxVIb5u0GMF+/YQYfXoWKTpeaj967k1+KHocTzVqsA53gb22/ogPiTShORAEuBbiNXRIbwtF2W7PKAEsSj7AKpcPOboK26ZzK3l8e0Bo/tQRHt5l1XJX+dnHvh2RsugDBN6erOfc35Yls/9Lq3QdNBjcUMMkLU6FOely63+1VpARRWpFGtj9MFEh7SzYXTpqtu5PkE8/ZsdyzCAapypYXChK/yl4nYY4W4yKs+AGiZrE3vzFAnPhE= root@mrofiq466

[VM]
NAME: demo-tvgen    # only use one word, use "-" if more one word
OS: template-ubuntu2004.img   # image on pool virsh
DHCP1: false    # true | false
DHCP2: true
DHCP3: false
DHCP4: false
VCPUS: 2
MEMORY: 4   # in GB
DISK1: 10   # in GB
DISK2: 10
IFACE_IP1: 10.10.110.10   # if dhcp1 is false set to fix ip
IFACE_IP2: default    # if dhcp2 is true set to name $(virsh net-list)
IFACE_IP3: 30.10.110.100  # use format ip class C (0.0.0.255)
IFACE_IP4: 40.10.110.100
CONSOLE: spice    # spice | vnc
```
