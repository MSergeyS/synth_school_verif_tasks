# synth_school_verif_tasks

для запуска (в Questa Sim)
```
make EXAMPLE=01_sum SIM_OPTS=-gui
```

кому не нравится квеста :) можно запустить на iverilog и gtkwave:
```
iverilog -g2005-sv -s testbench *.sv && echo finish | vvp ./a.out && gtkwave dump.vcd
```

Только не забудьте добавить $dumpvars; в тестбенче (testbench.sv)
```
        `ifdef __ICARUS__
        // Uncomment the following line
        // to generate a VCD file and analyze it using GTKwave or Surfer

            $dumpvars;
        `endif
```
