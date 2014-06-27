# vagrant-torque

Setup a single machine torque machine in a VM with Vagrant.

Useful for testing SCIENCE.

## Usage

Run locally:
```
vagrant up
vagrant ssh # connect to VM
```

Run on VM
```
# submit test job
qsub /vagrant/test.qsub

# check status
qstat

# check job output

cat test.qsub.*

# you should see Hello, World!
```

## License

Public Domain
