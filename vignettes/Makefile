default: all
RDIR = .
VIG_DRAFTS_DIR = $(RDIR)/drafts
RESOURCES = $(RDIR)/resources/*


analysis-template = $(VIG_DRAFTS_DIR)/analysis-template/analysis-template.html

all: $(analysis-template)

$(analysis-template): analysis-template.Rmd $(RESOURCES)
			R -e 'rmarkdown::render("analysis-template.Rmd", c("html_document", "word_document", "pdf_document"), output_dir = "drafts/analysis-template", output_options = list())'
