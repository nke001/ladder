##### MNIST 100 labels
```
# Full
run.py train --encoder-layers 1000-500-250-250-250-10 --decoder-spec sig --denoising-cost-x 1000,10,0.1,0.1,0.1,0.1,0.1 --labeled-samples 100 --unlabeled-samples 60000 --seed 1 -- mnist_100_full
# Bottom-only
run.py train --encoder-layers 1000-500-250-250-250-10 --decoder-spec sig --denoising-cost-x 4000,0,0,0,0,0,0 --labeled-samples 100 --unlabeled-samples 60000 --seed 1 -- mnist_100_bottom
# Gamma
run.py train --encoder-layers 1000-500-250-250-250-10 --decoder-spec 0-0-0-0-0-0-sig --denoising-cost-x 0,0,0,0,0,0,1 --labeled-samples 100 --unlabeled-samples 60000 --seed 1 -- mnist_100_gamma
# Supervised baseline
run.py train --encoder-layers 1000-500-250-250-250-10 --decoder-spec 0-0-0-0-0-0-0 --denoising-cost-x 0,0,0,0,0,0,0 --labeled-samples 100 --unlabeled-samples 60000 --f-local-noise-std 0.5 --seed 1 -- mnist_100_baseline
```

python run.py train --encoder-layers 300-1000-200-500-100-250-70-250-70-250-10 --decoder-spec sig-lin-sig-lin-sig-lin-sig-lin-sig-lin-sig-sig --denoising-cost-x 1000,0,10,0,0.1,0,0.1,0,0.1,0,0.1,0.1 --labeled-samples 100 --unlabeled-samples 50000 --valid-set-size 10000 --seed 1 -- mnist_100_BNL

