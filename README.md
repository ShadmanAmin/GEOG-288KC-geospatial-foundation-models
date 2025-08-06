# GEOG 288KC: Geospatial Foundation Models and Applications

**Fall 2025 | UC Santa Barbara**  
**Instructors:** Kelly Caylor (caylor@ucsb.edu) & Anna Boser (annaboser@ucsb.edu)  
**Website:** https://kellycaylor.github.io/geoAI

This repository contains the complete course materials, environment setup, and computational infrastructure for GEOG 288KC, a project-driven seminar on state-of-the-art geospatial foundation models for remote sensing and environmental monitoring.

## 👥 Repository Users

### For **Students**
- 🌐 **Course Website**: Visit https://kellycaylor.github.io/geoAI for all course content
- 📝 **Assignments**: Access via website navigation (projects, weekly materials)
- 💻 **Computing**: Use UCSB AI Sandbox following setup instructions in `installation/`

### For **Instructors** (Kelly Caylor & Anna Boser)
- 📚 **Course Development**: Edit content in `course-materials/`
- 🔧 **Website Updates**: Use `python build_docs.py --serve` for local development
- 📊 **Student Support**: Reference `installation/` for technical troubleshooting

### For **GRIT IT Support**
- 🖥️ **Environment Setup**: Use `installation/` directory for AI Sandbox configuration
- 🔧 **Troubleshooting**: See `installation/UCSB_AI_SANDBOX_SETUP.md` for detailed procedures
- 📞 **Contact**: Instructors available for technical consultation

## 🏗️ Repository Structure

```
geoAI/
├── 📚 course-materials/           # Course content (instructors edit here)
│   ├── week0.qmd - week10.qmd     # Weekly lesson materials
│   ├── projects/                  # Project templates and deliverables
│   ├── labs/                      # Hands-on lab sessions
│   ├── lectures/                  # Formal lecture content
│   └── resources/                 # Additional course resources
│
├── 🔧 installation/               # Environment & model setup (IT support)
│   ├── UCSB_AI_SANDBOX_SETUP.md  # Comprehensive setup guide
│   ├── environment-gpu.yml        # Conda environment specification
│   ├── requirements-gpu.txt       # Additional Python packages
│   └── scripts/                   # Automated installation scripts
│       ├── install_foundation_models.sh
│       ├── validate_environment.py
│       └── test_gpu_setup.py
│
├── 🌐 docs/                       # Generated website (auto-generated)
├── 📊 data/                       # Course datasets and samples
├── 🖼️ images/                     # Course imagery and assets
├── 📝 nbs/                        # Additional notebooks (not built)
│
├── 🔨 build_docs.py               # Website build script
├── ⚙️ _quarto.yml                 # Website configuration
├── 🌍 index.qmd                   # Course homepage
├── 📋 Syllabus.md                 # Course syllabus
├── 🐍 environment.yml             # Basic conda environment
└── 📄 requirements.txt            # Basic Python requirements
```

## 🚀 Quick Start Guides

### For Instructors: Course Development

```bash
# 1. Clone and setup repository
git clone https://github.com/kellycaylor/geoAI.git
cd geoAI

# 2. Create development environment
conda env create -f environment.yml
conda activate geoAI

# 3. Install additional packages
pip install -r requirements.txt

# 4. Start local development server
python build_docs.py --serve
# Website available at http://localhost:4200

# 5. Edit course materials in course-materials/
# 6. Commit and push changes to update website
```

### For GRIT IT Support: AI Sandbox Setup

```bash
# 1. SSH to AI Sandbox
ssh username@ai-sandbox.ucsb.edu

# 2. Clone course repository
git clone https://github.com/kellycaylor/geoAI.git
cd geoAI

# 3. Run automated setup
bash installation/scripts/install_foundation_models.sh

# 4. Validate installation
python installation/scripts/validate_environment.py

# 5. Test GPU acceleration
python installation/scripts/test_gpu_setup.py
```

### For Students: Getting Started

1. **Access Course Website**: https://kellycaylor.github.io/geoAI
2. **Request AI Sandbox Access**: Follow instructions in Week 0 materials
3. **Complete Environment Setup**: Use provided installation scripts
4. **Submit Project Application**: Via course website form

## 💻 Technical Requirements

### AI Sandbox Specifications
- **GPU**: NVIDIA A100/H100 (recommended) or V100 (minimum)
- **RAM**: 32GB+ system memory
- **Storage**: 100GB+ for models and datasets
- **CUDA**: 11.8 or 12.1 
- **Python**: 3.11 with conda/mamba

### Foundation Models Included
- **Prithvi-100M**: NASA-IBM Earth observation foundation model (~2GB)
- **SatMAE**: Microsoft satellite masked autoencoder (~1GB)
- **CLIP**: OpenAI vision-language models (~1GB each)
- **Additional Models**: Domain-specific geospatial models (~5GB total)

### Key Software Packages
- **PyTorch 2.1+**: GPU-accelerated deep learning
- **TorchGeo**: Geospatial machine learning library
- **HuggingFace**: Foundation model access and fine-tuning
- **Earth Engine**: Large-scale satellite data analysis
- **GDAL/Rasterio**: Geospatial data processing

## 📚 Course Overview

### Learning Objectives
Students will master:
- **Foundation Model Theory**: Understanding of self-supervised learning and transformer architectures
- **Geospatial Applications**: Fine-tuning models for Earth observation tasks
- **Scalable Pipelines**: Cloud-based analysis using Earth Engine and distributed computing
- **Model Deployment**: Building APIs and interactive applications
- **Project Development**: Applied research with real-world geospatial problems

### Assessment Structure
- **Pass/Fail**: Based on attendance, participation, and deliverable submission
- **Project Application** (Week 0): Research interest and background
- **Project Proposal** (Week 3): Detailed technical plan
- **Initial MVP** (Week 7): Working prototype demonstration
- **Final Presentation** (Week 10): Complete project showcase

### Weekly Schedule
| Week | Topic | Focus |
|------|-------|-------|
| 0 | Getting Started | AI Sandbox setup, project applications |
| 1-2 | Foundation Models | Theory, data handling, model outputs |
| 3-4 | Fine-tuning & Multi-modal | Adaptation techniques, generative models |
| 5-6 | Project Development | Independent work, evaluation strategies |
| 7-8 | Scalable Deployment | Cloud pipelines, APIs, applications |
| 9-10 | Synthesis & Presentations | Project completion, final demonstrations |

## 🔧 Development Workflow

### For Instructors

#### Content Updates
```bash
# 1. Edit course materials
vim course-materials/week1.qmd

# 2. Preview changes locally
python build_docs.py --serve

# 3. Build for production
python build_docs.py --full

# 4. Commit and push
git add .
git commit -m "Update Week 1 content"
git push origin main
```

#### Adding New Models
```bash
# 1. Update installation script
vim installation/scripts/install_foundation_models.sh

# 2. Test installation
bash installation/scripts/install_foundation_models.sh

# 3. Update documentation
vim installation/UCSB_AI_SANDBOX_SETUP.md

# 4. Create usage examples
vim course-materials/labs/new_model_example.qmd
```

### For GRIT Support

#### Environment Maintenance
```bash
# Check environment health
python installation/scripts/validate_environment.py

# Update packages
conda env update -f installation/environment-gpu.yml
pip install -r installation/requirements-gpu.txt --upgrade

# Monitor resource usage
nvidia-smi
df -h
```

#### Troubleshooting Common Issues
1. **CUDA/GPU Issues**: Check `installation/UCSB_AI_SANDBOX_SETUP.md` Section 6
2. **Model Download Failures**: Verify HuggingFace authentication
3. **Memory Errors**: Adjust batch sizes in example code
4. **Earth Engine Authentication**: Re-run `earthengine authenticate`

## 📞 Support Contacts

### Course Instructors
- **Kelly Caylor** (caylor@ucsb.edu): Course lead, technical architecture
- **Anna Boser** (annaboser@ucsb.edu): Teaching assistant, student support

### Technical Support
- **UCSB GRIT**: AI Sandbox infrastructure and GPU access
- **GitHub Issues**: https://github.com/kellycaylor/geoAI/issues
- **Course Slack**: Real-time technical support during course

### Office Hours
- **Instructor Office Hours**: By appointment
- **Technical Lab Sessions**: Fridays 2-5pm (optional)
- **GRIT Support**: Via ticket system at grit.ucsb.edu

## 📜 License and Usage

- **Course Materials**: Creative Commons Attribution 4.0 International
- **Code Examples**: MIT License
- **Foundation Models**: Subject to individual model licenses (see installation scripts)
- **Student Projects**: Owned by students, optional public sharing encouraged

## 🚨 Important Notes

### For IT Support
- **Resource Intensive**: Foundation models require significant GPU memory and storage
- **Network Bandwidth**: Initial setup involves ~15-20GB of downloads
- **User Authentication**: Students need HuggingFace accounts for model access
- **Monitoring**: GPU usage monitoring recommended during peak course periods

### For Instructors
- **Model Updates**: Foundation models evolve rapidly; review quarterly
- **Student Diversity**: Expect varying technical backgrounds; provide multiple entry points
- **Project Scope**: Help students balance ambition with 10-week timeline constraints
- **Resource Allocation**: Coordinate with GRIT for peak usage periods

### For Students
- **Early Setup**: Begin AI Sandbox setup immediately after enrollment
- **Regular Backups**: Save work frequently; use version control
- **Resource Awareness**: Be mindful of GPU usage during shared access periods
- **Academic Integrity**: Properly cite model sources and collaborations

---

**Repository Maintainers**: Kelly Caylor & Anna Boser  
**Last Updated**: August 2025  
**Course Website**: https://kellycaylor.github.io/geoAI