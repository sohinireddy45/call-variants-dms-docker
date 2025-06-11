

# call-variants-dms-docker

---

## Purpose & Credits

This repository provides a **Dockerized version** of the `call_variants.py` workflow from the [barakcohenlab/crx-dms-manuscript](https://github.com/barakcohenlab/crx-dms-manuscript) repository.

> **Original authorship and implementation** of the variant-calling logic belongs to James Gagnon and the Barak Cohen Lab.  
> This repository **does not modify or reinterpret** the core logic.  
> Our lab's contribution was to **containerize** the environment (Python + Rust) and make the pipeline **reproducible** for HPC use.

---

##  Usage Instructions

### 1. The container
```bash
docker pull sohinireddy0205/call-variants-dms-base:latest
````

### 2. Required inputs

* A `.paf` file generated from PacBio HiFi reads aligned with `minimap2`
* A `call_variants_changable.py` script (included or customized)

### 3. Run (example for HPC with LSF)

```bash
     python3 /mnt/call_variants_changable.py \
             /mnt/input.paf \
             /mnt/barcode_variant_map.tsv
```
