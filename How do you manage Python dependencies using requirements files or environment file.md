### **Interview‑Style Answer: How do you manage Python dependencies using requirements files or environment files?**

I manage Python dependencies by **isolating environments** and **explicitly locking dependencies** so applications run consistently across development, testing, and production.

Typically, I use a **virtual environment** (such as `venv` or `virtualenv`) to isolate project‑specific dependencies. All required Python packages and their versions are listed in a **`requirements.txt` file**, which serves as the single source of truth for dependencies. This file is generated using `pip freeze` and allows anyone to recreate the exact environment using `pip install -r requirements.txt`.

For more advanced dependency and environment management, I may use **environment files or tools** like Pipenv or Poetry. These tools separate:

*   **Application dependencies** from
*   **Development or testing dependencies**,  
    and lock exact versions using files like `Pipfile.lock` or `poetry.lock`.

In CI/CD pipelines, dependencies are always installed from these locked files, ensuring **reproducible builds**. Environment‑specific settings (like secrets or configuration values) are handled separately using `.env` files or environment variables, not hard‑coded into dependency files.

### **Example**

*   Developer adds a library → updates `requirements.txt`
*   CI pipeline installs dependencies using that file
*   The same dependency versions are used in staging and production

### **One‑line interview summary**

> *I manage Python dependencies by using isolated virtual environments and locked dependency files like `requirements.txt` or environment‑based tools to ensure consistent and reproducible builds across all environments.*

If you want, I can also:

*   Compare **requirements.txt vs Pipenv vs Poetry**
*   Explain **best practices in CI/CD**
*   Give an **example project structure**
