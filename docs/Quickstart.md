
# 🚀 Quickstart: Running Symbion

This guide will help you run the Symbion framework locally and simulate your first policy.

---

## 📦 Prerequisites

- [.NET SDK](https://dotnet.microsoft.com/en-us/download) (v7 or later)
- [Node.js](https://nodejs.org/) (for frontend UI)
- [Git](https://git-scm.com/)
- Optional: Docker, PlantUML, Java (for diagram rendering)

---

## 🧠 Step 1: Clone the Repo

```bash
git clone https://github.com/your-username/symbion.git
cd symbion
```

---

## 🛠️ Step 2: Run the Backend

```bash
cd core
dotnet build
dotnet run
```

This starts the core API at `http://localhost:5000`.

---

## 🌐 Step 3: Run the Frontend UI (Optional)

```bash
cd ui/symbion-ui
npm install
npm run dev
```

Visit `http://localhost:3000` to interact with the simulation UI.

---

## 🧪 Step 4: Simulate a Policy

You can use a DSL policy like this one:

```yaml
id: policy.education.investment
name: "Increase Education Funding"
targets:
  - resource: Education
    change: { budget: "+10%" }
effects:
  - from: Education
    to: Employment
    weight: 0.7
    delay: "6 months"
```

Save it to: `plugins/dsl/education_investment.yaml`

Then use the CLI (or UI) to simulate:

```bash
dotnet run -- simulate --policy plugins/dsl/education_investment.yaml
```

---

## ✅ Next Steps

- Explore `/examples/` for more policies
- Contribute new resources or relationships
- Join discussions or open issues

