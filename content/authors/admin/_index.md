---
# Display name
name: Fuhrman Lab 

# Username (this should match the folder name)
authors:
- admin

# Is this the primary user of the site?
superuser: true

# Role/position
role: Marine Microbial Ecologists

# Organizations/Affiliations
organizations:
- name: University of Southern California
  url: ""

# Short bio (displayed in user profile at end of posts)
bio: Research in the Fuhrman Lab focuses on microbial biodiversity and how viruses, bacteria, archaea, protists, and primary producers interact to shape the network of microorganisms functioning in the marine environment.

interests:
- Microbial Ecology
- Methods Development and Validation
- Interactions and Networks


# Social/Academic Networking
# For available icons, see: https://sourcethemes.com/academic/docs/widgets/#icons
#   For an email link, use "fas" icon pack, "envelope" icon, and a link in the
#   form "mailto:your-email@example.com" or "#contact" for contact widget.
social:
- icon: twitter
  icon_pack: fab
  link: https://twitter.com/jedfuhrman?lang=en
- icon: google-scholar
  icon_pack: ai
  link: https://scholar.google.com.hk/citations?hl=en&user=VjvupJUAAAAJ&view_op=list_works&sortby=pubdate
- icon: github
  icon_pack: fab
  link: https://github.com/fuhrmanlab
# Link to a PDF of your resume/CV from the About widget.
# To enable, copy your resume/CV to `static/files/cv.pdf` and uncomment the lines below.  
# - icon: cv
#   icon_pack: ai
#   link: files/cv.pdf

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ""

# Organizational groups that you belong to (for People widget)
#   Set this to `[]` or comment out if you are not using People widget.  
user_groups:
- Researchers
- Visitors
---

Research in the Fuhrman Lab focuses on microbial biodiversity and how viruses, bacteria, archaea, protists, and primary producers interact to shape the network of microorganisms functioning in the marine environment. Using field and laboratory experiments in conjunction with molecular, bioinformatic, and statistical tools, we investigate temporal and spatial patterns of microbial productivity and diversity, taking advantage of over 18 years of monthly data from our USC Microbial Observatory at the San Pedro Ocean Time Series (SPOT) as well as other data from around the world. Ongoing research emphasizes the roles of microbial interactions, including those with viruses and protists, on shaping the bacterial and archaeal populations, specifically seeking to link particular organisms within their complex network of associations.

This website is a central repository for sharing active protocols, both within the Fuhrman lab and to the oustide world. Of particular note are our protocols for the sequencing of PCR amplicons with *truly universal* SSU rRNA primers (515Y/926R) that generate amplicons from both 16S and 18S sequences. In practical terms, this means that from a single DNA extract, one can profile the cellular community from **A**rchaea to meta**Z**oa. We have also developed a set of scripts that use qiime2 to process the data in a manner specific to these universal primers. In brief, the pipeline splits 16S and 18S informatically (using bbsplit) then denoises with either DADA2 or deblur, then slices and dices the data according to several preset categories. We have also recently included ways to get more information on poorly classified sequences by tweaking parameters in the classification algorithm. The whole pipleine is meant to simplify the process of using qiime2 so that the user has more time to do the important interpretation work that comes after the data have been processed.
