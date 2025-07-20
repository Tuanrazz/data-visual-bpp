<img src="https://g.top4top.io/p_3488xrwpp5.jpg" width="100%" />

**ini adalah visualisasi data buku penggaris dan pulpen, menggunakan library numpy, matplotlib dan pandas**

**untuk code nya seperti ini:**

```'''script tuanrazz,
 jangan lupa follow'''

import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

# 1. data
np.random.seed(42)
tanggal = pd.date_range("2025-07-20", periods=12, freq="M")
data = {
    "Buku": np.random.randint(20, 50, size=12).cumsum(),
    "penggaris": np.random.randint(10, 40, size=12).cumsum(),
    "Pulpen": np.random.randint(5, 30,  size=12).cumsum(),
}
df = pd.DataFrame(data, index=tanggal)

# 2. garis area
ax = df.plot(kind="area", figsize=(10, 6), alpha=0.7, linewidth=0)

# 3. menghias
ax.set_title("Penjualan Produk per Bulan", fontsize=7, weight="bold")
ax.set_xlabel("Bulan")
ax.set_ylabel("Total Penjualan")
ax.grid(axis="y", linestyle="--", alpha=0.3)
plt.tight_layout()
plt.show()

