
# parsec3-patch
Parsec 3.0 Benchmark Suite Patches on AlmaLinux/RockyLinux 9

# Build
Download the full parsec 3.0 from Princeton University Website
```shell
wget http://parsec.cs.princeton.edu/download/3.0/parsec-3.0.tar.gz
```

Clone parsec3 patch repo and apply these patches
```shell
git clone https://github.com/markyangcc/parsec3-patch.git

for file in parsec3-patch/*.patch; do patch -p1 < "$file"; done
```

Build parsec benchmark suite
```shell
source env.sh
parsecmgmt -a build
```

