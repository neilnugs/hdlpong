# hdlpong
These designs make use of modules from the Project F library.

Made using Verilator and System Verilog.

## Building and running

Can use this to build pong game:

```bash
cd pong/sim

verilator -I../ -cc top_pong.sv --exe main_pong.cpp -o pong \
    -CFLAGS "$(sdl2-config --cflags)" -LDFLAGS "$(sdl2-config --libs)"

make -C ./obj_dir -f Vtop_pong.mk
```
or, alternatively, the makefile could also be used:

```bash
make pong
```

And then run the simulation executable from obj_dir:
```bash
./obj_dir/pong
```

## Snippet of Pong in SystemVerilog in Verilator Simulation
![Pong game in SystemVerilog!](doc/img/pong.png?raw=true "")

## Next in line in my HDL journey:
- find out a sound extension that can be used for verilog simulators and model dsp algorithms
