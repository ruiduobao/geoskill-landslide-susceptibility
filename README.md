# geoskill-landslide-susceptibility

> Integrate terrain, geology, rainfall, land cover, roads, and historical landslide data to produce interpretable susceptibility zoning with spatial cross-validation.

See [SKILL.md](SKILL.md) for full usage, inputs and outputs.

## Quick start

```bash
# Synthetic demo mode (no input files needed)
python scripts/landslide_susceptibility.py --output-dir ./ls-output

# With custom model
python scripts/landslide_susceptibility.py --model random_forest --output-dir ./ls-output

# With custom parameters
python scripts/landslide_susceptibility.py \
  --model logistic_regression \
  --negative-sampling buffer \
  --cv-block-size 20 \
  --n-folds 5 \
  --class-schema five_class \
  --output-dir ./ls-output

# With custom factor config
python scripts/landslide_susceptibility.py \
  --factor-config ./my-factor-config.json \
  --output-dir ./ls-output
```

## License

MIT
