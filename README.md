# Bioinformatics-pipeline

# Upload file
def upload_to_gcs(bucket_name, source_file_path, destination_blob_name):
    client = storage.Client()
    bucket = client.bucket(bucket_name)
    blob = bucket.blob(destination_blob_name)
    blob.upload_from_filename(source_file_path)
    print(f"File {source_file_path} uploaded to gs://{bucket_name}/{destination_blob_name}.")

upload_to_gcs(bucket_name, source_file_path, destination_blob_name)
-bash: from: command not found
-bash: import: command not found
-bash: bucket_name: command not found
-bash: syntax error near unexpected token `('
-bash: destination_blob_name: command not found
-bash: os.environ[GOOGLE_APPLICATION_CREDENTIALS]: command not found
-bash: syntax error near unexpected token `('
-bash: syntax error near unexpected token `('
-bash: syntax error near unexpected token `('
-bash: syntax error near unexpected token `('
-bash: syntax error near unexpected token `source_file_path'
-bash: syntax error near unexpected token `f"File {source_file_path} uploaded to gs://{bucket_name}/{destination_blob_name}."'
-bash: syntax error near unexpected token `bucket_name,'
(base) tofio17794@cs-929994200285-default:~/bio_info$ fastqc
-bash: fastqc: command not found
(base) tofio17794@cs-929994200285-default:~/bio_info$ wget https://drive.google.com/drive/folders/1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=sharing
--2025-06-19 16:42:14--  https://drive.google.com/drive/folders/1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=sharing
Resolving drive.google.com (drive.google.com)... 142.251.168.102, 142.251.168.139, 142.251.168.101, ...
Connecting to drive.google.com (drive.google.com)|142.251.168.102|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: ‘1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=sharing’

1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=s     [ <=>                                                                          ] 257.78K  1.30MB/s    in 0.2s    

2025-06-19 16:42:14 (1.30 MB/s) - ‘1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=sharing’ saved [263970]

(base) tofio17794@cs-929994200285-default:~/bio_info$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       628Mi       5.3Gi       1.1Mi       2.1Gi       7.1Gi
Swap:             0B          0B          0B
(base) tofio17794@cs-929994200285-default:~/bio_info$ wget https://drive.google.com/file/d/1tj0UZ16ufcSmcYfObK0svFZBsPHXtco6/view?usp=drive_link
--2025-06-19 16:50:47--  https://drive.google.com/file/d/1tj0UZ16ufcSmcYfObK0svFZBsPHXtco6/view?usp=drive_link
Resolving drive.google.com (drive.google.com)... 142.251.168.101, 142.251.168.100, 142.251.168.102, ...
Connecting to drive.google.com (drive.google.com)|142.251.168.101|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: ‘view?usp=drive_link’

view?usp=drive_link                         [ <=>                                                                          ]  98.32K  --.-KB/s    in 0.02s   

2025-06-19 16:50:48 (4.36 MB/s) - ‘view?usp=drive_link’ saved [100681]

(base) tofio17794@cs-929994200285-default:~/bio_info$ ls
'1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=sharing'   Miniconda3-latest-Linux-x86_64.sh  'view?usp=drive_link'
(base) tofio17794@cs-929994200285-default:~/bio_info$ pip install gdown
Collecting gdown
  Downloading gdown-5.2.0-py3-none-any.whl.metadata (5.8 kB)
Collecting beautifulsoup4 (from gdown)
  Downloading beautifulsoup4-4.13.4-py3-none-any.whl.metadata (3.8 kB)
Collecting filelock (from gdown)
  Downloading filelock-3.18.0-py3-none-any.whl.metadata (2.9 kB)
Requirement already satisfied: requests[socks] in /home/tofio17794/miniconda3/lib/python3.13/site-packages (from gdown) (2.32.3)
Requirement already satisfied: tqdm in /home/tofio17794/miniconda3/lib/python3.13/site-packages (from gdown) (4.67.1)
Collecting soupsieve>1.2 (from beautifulsoup4->gdown)
  Downloading soupsieve-2.7-py3-none-any.whl.metadata (4.6 kB)
Requirement already satisfied: typing-extensions>=4.0.0 in /home/tofio17794/miniconda3/lib/python3.13/site-packages (from beautifulsoup4->gdown) (4.12.2)
Requirement already satisfied: charset-normalizer<4,>=2 in /home/tofio17794/miniconda3/lib/python3.13/site-packages (from requests[socks]->gdown) (3.3.2)
Requirement already satisfied: idna<4,>=2.5 in /home/tofio17794/miniconda3/lib/python3.13/site-packages (from requests[socks]->gdown) (3.7)
Requirement already satisfied: urllib3<3,>=1.21.1 in /home/tofio17794/miniconda3/lib/python3.13/site-packages (from requests[socks]->gdown) (2.3.0)
Requirement already satisfied: certifi>=2017.4.17 in /home/tofio17794/miniconda3/lib/python3.13/site-packages (from requests[socks]->gdown) (2025.4.26)
Requirement already satisfied: PySocks!=1.5.7,>=1.5.6 in /home/tofio17794/miniconda3/lib/python3.13/site-packages (from requests[socks]->gdown) (1.7.1)
Downloading gdown-5.2.0-py3-none-any.whl (18 kB)
Downloading beautifulsoup4-4.13.4-py3-none-any.whl (187 kB)
Downloading filelock-3.18.0-py3-none-any.whl (16 kB)
Downloading soupsieve-2.7-py3-none-any.whl (36 kB)
Installing collected packages: soupsieve, filelock, beautifulsoup4, gdown
Successfully installed beautifulsoup4-4.13.4 filelock-3.18.0 gdown-5.2.0 soupsieve-2.7
(base) tofio17794@cs-929994200285-default:~/bio_info$ wget https://drive.google.com/file/d/1tj0UZ16ufcSmcYfObK0svFZBsPHXtco6/view?usp=drive_link^C
(base) tofio17794@cs-929994200285-default:~/bio_info$ gdown --id 1tj0UZ16ufcSmcYfObK0svFZBsPHXtco6
/home/tofio17794/miniconda3/lib/python3.13/site-packages/gdown/__main__.py:140: FutureWarning: Option `--id` was deprecated in version 4.3.1 and will be removed in 5.0. You don't need to pass it anymore to use a file ID.
  warnings.warn(
Downloading...
From (original): https://drive.google.com/uc?id=1tj0UZ16ufcSmcYfObK0svFZBsPHXtco6
From (redirected): https://drive.google.com/uc?id=1tj0UZ16ufcSmcYfObK0svFZBsPHXtco6&confirm=t&uuid=6498e34b-f78a-47df-9286-3e4601ea415b
To: /home/tofio17794/bio_info/LG_BM_MK_PR_001_S35_R1_001.fastq.gz
100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1.78G/1.78G [00:32<00:00, 54.0MB/s]
(base) tofio17794@cs-929994200285-default:~/bio_info$ gdown --id 1_bCnn_1r4P5KWggaJaN8CALI-3ELoEbR
/home/tofio17794/miniconda3/lib/python3.13/site-packages/gdown/__main__.py:140: FutureWarning: Option `--id` was deprecated in version 4.3.1 and will be removed in 5.0. You don't need to pass it anymore to use a file ID.
  warnings.warn(
Downloading...
From (original): https://drive.google.com/uc?id=1_bCnn_1r4P5KWggaJaN8CALI-3ELoEbR
From (redirected): https://drive.google.com/uc?id=1_bCnn_1r4P5KWggaJaN8CALI-3ELoEbR&confirm=t&uuid=70796afb-8b1c-4321-8837-d6fa893f9989
To: /home/tofio17794/bio_info/LG_BM_MK_PR_001_S35_R2_001.fastq.gz
100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1.87G/1.87G [00:17<00:00, 106MB/s]
(base) tofio17794@cs-929994200285-default:~/bio_info$ conda install -c bioconda fastqc
Channels:
 - bioconda
 - defaults
Platform: linux-64
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/tofio17794/miniconda3

  added / updated specs:
    - fastqc


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    cairo-1.16.0               |       he5ede1b_6         1.2 MB
    conda-25.5.1               |  py313h06a4308_0         1.2 MB
    dbus-1.13.18               |       hb2f20db_0         504 KB
    fastqc-0.12.1              |       hdfd78af_0        11.1 MB  bioconda
    font-ttf-dejavu-sans-mono-2.37|       hd3eb1b0_0         335 KB
    fontconfig-2.14.1          |       h55d465d_3         281 KB
    freetype-2.13.3            |       h4a9f257_0         686 KB
    fribidi-1.0.10             |       h7b6447c_0         103 KB
    glib-2.78.4                |       h6a678d5_0         508 KB
    glib-tools-2.78.4          |       h6a678d5_0         115 KB
    graphite2-1.3.14           |       h295c915_1          97 KB
    harfbuzz-10.2.0            |       hdfddeaa_1         2.3 MB
    libglib-2.78.4             |       hdc74915_0         1.5 MB
    libiconv-1.16              |       h5eee18b_3         759 KB
    libpng-1.6.39              |       h5eee18b_0         304 KB
    libxcb-1.17.0              |       h9b100fa_0         430 KB
    openjdk-21.0.6             |       h38aa4c6_0       393.0 MB
    pango-1.50.7               |       h668f713_2         474 KB
    perl-5.40.2                | 0_h5eee18b_perl5        13.2 MB
    pixman-0.40.0              |       h7f8727e_1         373 KB
    pthread-stubs-0.3          |       h0ce48e5_1           5 KB
    xorg-libx11-1.8.12         |       h9b100fa_1         895 KB
    xorg-libxau-1.0.12         |       h9b100fa_0          13 KB
    xorg-libxdmcp-1.1.5        |       h9b100fa_0          19 KB
    xorg-libxext-1.3.6         |       h9b100fa_0          49 KB
    xorg-libxrender-0.9.12     |       h9b100fa_0          31 KB
    xorg-xorgproto-2024.1      |       h5eee18b_1         580 KB
    ------------------------------------------------------------
                                           Total:       429.9 MB

The following NEW packages will be INSTALLED:

  cairo              pkgs/main/linux-64::cairo-1.16.0-he5ede1b_6 
  dbus               pkgs/main/linux-64::dbus-1.13.18-hb2f20db_0 
  fastqc             bioconda/noarch::fastqc-0.12.1-hdfd78af_0 
  font-ttf-dejavu-s~ pkgs/main/noarch::font-ttf-dejavu-sans-mono-2.37-hd3eb1b0_0 
  fontconfig         pkgs/main/linux-64::fontconfig-2.14.1-h55d465d_3 
  freetype           pkgs/main/linux-64::freetype-2.13.3-h4a9f257_0 
  fribidi            pkgs/main/linux-64::fribidi-1.0.10-h7b6447c_0 
  glib               pkgs/main/linux-64::glib-2.78.4-h6a678d5_0 
  glib-tools         pkgs/main/linux-64::glib-tools-2.78.4-h6a678d5_0 
  graphite2          pkgs/main/linux-64::graphite2-1.3.14-h295c915_1 
  harfbuzz           pkgs/main/linux-64::harfbuzz-10.2.0-hdfddeaa_1 
  libglib            pkgs/main/linux-64::libglib-2.78.4-hdc74915_0 
  libiconv           pkgs/main/linux-64::libiconv-1.16-h5eee18b_3 
  libpng             pkgs/main/linux-64::libpng-1.6.39-h5eee18b_0 
  libxcb             pkgs/main/linux-64::libxcb-1.17.0-h9b100fa_0 
  openjdk            pkgs/main/linux-64::openjdk-21.0.6-h38aa4c6_0 
  pango              pkgs/main/linux-64::pango-1.50.7-h668f713_2 
  perl               pkgs/main/linux-64::perl-5.40.2-0_h5eee18b_perl5 
  pixman             pkgs/main/linux-64::pixman-0.40.0-h7f8727e_1 
  pthread-stubs      pkgs/main/linux-64::pthread-stubs-0.3-h0ce48e5_1 
  xorg-libx11        pkgs/main/linux-64::xorg-libx11-1.8.12-h9b100fa_1 
  xorg-libxau        pkgs/main/linux-64::xorg-libxau-1.0.12-h9b100fa_0 
  xorg-libxdmcp      pkgs/main/linux-64::xorg-libxdmcp-1.1.5-h9b100fa_0 
  xorg-libxext       pkgs/main/linux-64::xorg-libxext-1.3.6-h9b100fa_0 
  xorg-libxrender    pkgs/main/linux-64::xorg-libxrender-0.9.12-h9b100fa_0 
  xorg-xorgproto     pkgs/main/linux-64::xorg-xorgproto-2024.1-h5eee18b_1 

The following packages will be UPDATED:

  conda                              25.3.1-py313h06a4308_0 --> 25.5.1-py313h06a4308_0 


Proceed ([y]/n)? y


Downloading and Extracting Packages:
                                                                                                                                                              
                                                                                                                                                              
CondaError: Failed to write to /home/tofio17794/miniconda3/pkgs/fontconfig-2.14.1-h55d465d_3.conda.partial                                                    
  errno: 28                                                                                                                                                   
CondaError: Failed to write to /home/tofio17794/miniconda3/pkgs/libpng-1.6.39-h5eee18b_0.conda.partial                                                        
  errno: 28                                                                                                                                                   
CondaError: Failed to write to /home/tofio17794/miniconda3/pkgs/fontconfig-2.14.1-h55d465d_3.conda.partial                                                    
  errno: 28                                                                                                                                                   
CondaError: Failed to write to /home/tofio17794/miniconda3/pkgs/openjdk-21.0.6-h38aa4c6_0.conda.partial                                                       
  errno: 28                                                                                                                                                   
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/harfbuzz-10.2.0-hdfddeaa_1.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')                                                                    
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/conda-25.5.1-py313h06a4308_0.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')                                                                  
InvalidArchiveError("Error with archive /home/tofio17794/miniconda3/pkgs/libiconv-1.16-h5eee18b_3.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device: '/home/tofio17794/miniconda3/pkgs/libiconv-1.16-h5eee18b_3/info/recipe'")                                                                                                                                                           
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/xorg-libx11-1.8.12-h9b100fa_1.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')                                                                 
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/freetype-2.13.3-h4a9f257_0.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')                                                                    
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/dbus-1.13.18-hb2f20db_0.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')                                                                       
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/xorg-xorgproto-2024.1-h5eee18b_1.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')                                                              
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/pango-1.50.7-h668f713_2.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/glib-2.78.4-h6a678d5_0.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/font-ttf-dejavu-sans-mono-2.37-hd3eb1b0_0.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')
InvalidArchiveError('Error with archive /home/tofio17794/miniconda3/pkgs/libxcb-1.17.0-h9b100fa_0.conda.  You probably need to delete and re-download or re-create this file.  Message was:\n\nfailed with error: [Errno 28] No space left on device')

(base) tofio17794@cs-929994200285-default:~/bio_info$ free -h
               total        used        free      shared  buff/cache   available
Mem:           7.8Gi       689Mi       2.6Gi       1.1Mi       4.8Gi       7.1Gi
Swap:             0B          0B          0B
(base) tofio17794@cs-929994200285-default:~/bio_info$ rm -r 
rm: missing operand
Try 'rm --help' for more information.
(base) tofio17794@cs-929994200285-default:~/bio_info$ ls
'1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=sharing'   LG_BM_MK_PR_001_S35_R2_001.fastq.gz  'view?usp=drive_link'
 LG_BM_MK_PR_001_S35_R1_001.fastq.gz              Miniconda3-latest-Linux-x86_64.sh
(base) tofio17794@cs-929994200285-default:~/bio_info$ rm -r ^C
(base) tofio17794@cs-929994200285-default:~/bio_info$ ^C
(base) tofio17794@cs-929994200285-default:~/bio_info$  rm -r LG_BM_MK_PR_001_S35_R2_001.fastq.gz 
(base) tofio17794@cs-929994200285-default:~/bio_info$ LS
-bash: LS: command not found
(base) tofio17794@cs-929994200285-default:~/bio_info$ ls
'1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=sharing'   LG_BM_MK_PR_001_S35_R1_001.fastq.gz   Miniconda3-latest-Linux-x86_64.sh  'view?usp=drive_link'
(base) tofio17794@cs-929994200285-default:~/bio_info$ conda install -c bioconda trimmomatic
Channels:
 - bioconda
 - defaults
Platform: linux-64
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/tofio17794/miniconda3

  added / updated specs:
    - trimmomatic


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    fontconfig-2.14.1          |       h55d465d_3         281 KB
    fribidi-1.0.10             |       h7b6447c_0         103 KB
    glib-tools-2.78.4          |       h6a678d5_0         115 KB
    graphite2-1.3.14           |       h295c915_1          97 KB
    libpng-1.6.39              |       h5eee18b_0         304 KB
    openjdk-21.0.6             |       h38aa4c6_0       393.0 MB
    pthread-stubs-0.3          |       h0ce48e5_1           5 KB
    trimmomatic-0.39           |       hdfd78af_2         144 KB  bioconda
    xorg-libxau-1.0.12         |       h9b100fa_0          13 KB
    xorg-libxdmcp-1.1.5        |       h9b100fa_0          19 KB
    xorg-libxext-1.3.6         |       h9b100fa_0          49 KB
    xorg-libxrender-0.9.12     |       h9b100fa_0          31 KB
    ------------------------------------------------------------
                                           Total:       394.1 MB

The following NEW packages will be INSTALLED:

  cairo              pkgs/main/linux-64::cairo-1.16.0-he5ede1b_6 
  dbus               pkgs/main/linux-64::dbus-1.13.18-hb2f20db_0 
  fontconfig         pkgs/main/linux-64::fontconfig-2.14.1-h55d465d_3 
  freetype           pkgs/main/linux-64::freetype-2.13.3-h4a9f257_0 
  fribidi            pkgs/main/linux-64::fribidi-1.0.10-h7b6447c_0 
  glib               pkgs/main/linux-64::glib-2.78.4-h6a678d5_0 
  glib-tools         pkgs/main/linux-64::glib-tools-2.78.4-h6a678d5_0 
  graphite2          pkgs/main/linux-64::graphite2-1.3.14-h295c915_1 
  harfbuzz           pkgs/main/linux-64::harfbuzz-10.2.0-hdfddeaa_1 
  libglib            pkgs/main/linux-64::libglib-2.78.4-hdc74915_0 
  libiconv           pkgs/main/linux-64::libiconv-1.16-h5eee18b_3 
  libpng             pkgs/main/linux-64::libpng-1.6.39-h5eee18b_0 
  libxcb             pkgs/main/linux-64::libxcb-1.17.0-h9b100fa_0 
  openjdk            pkgs/main/linux-64::openjdk-21.0.6-h38aa4c6_0 
  pango              pkgs/main/linux-64::pango-1.50.7-h668f713_2 
  pixman             pkgs/main/linux-64::pixman-0.40.0-h7f8727e_1 
  pthread-stubs      pkgs/main/linux-64::pthread-stubs-0.3-h0ce48e5_1 
  trimmomatic        bioconda/noarch::trimmomatic-0.39-hdfd78af_2 
  xorg-libx11        pkgs/main/linux-64::xorg-libx11-1.8.12-h9b100fa_1 
  xorg-libxau        pkgs/main/linux-64::xorg-libxau-1.0.12-h9b100fa_0 
  xorg-libxdmcp      pkgs/main/linux-64::xorg-libxdmcp-1.1.5-h9b100fa_0 
  xorg-libxext       pkgs/main/linux-64::xorg-libxext-1.3.6-h9b100fa_0 
  xorg-libxrender    pkgs/main/linux-64::xorg-libxrender-0.9.12-h9b100fa_0 
  xorg-xorgproto     pkgs/main/linux-64::xorg-xorgproto-2024.1-h5eee18b_1 

The following packages will be UPDATED:

  conda                              25.3.1-py313h06a4308_0 --> 25.5.1-py313h06a4308_0 


Proceed ([y]/n)? y


Downloading and Extracting Packages:
                                                                                                                                                              
Preparing transaction: done                                                                                                                                   
Verifying transaction: done                                                                                                                                   
Executing transaction: done                                                                                                                                   
(base) tofio17794@cs-929994200285-default:~/bio_info$ trimmomatic PE -phred33 
Usage:                                                                                                                                                        
       PE [-version] [-threads <threads>] [-phred33|-phred64] [-trimlog <trimLogFile>] [-summary <statsSummaryFile>] [-quiet] [-validatePairs] [-basein <inputBase> | <inputFile1> <inputFile2>] [-baseout <outputBase> | <outputFile1P> <outputFile1U> <outputFile2P> <outputFile2U>] <trimmer1>...                        
   or:                                                                                                                                                        
       SE [-version] [-threads <threads>] [-phred33|-phred64] [-trimlog <trimLogFile>] [-summary <statsSummaryFile>] [-quiet] <inputFile> <outputFile> <trimmer1>...                                                                                                                                                        
   or:                                                                                                                                                        
       -version
(base) tofio17794@cs-929994200285-default:~/bio_info$ trimmomatic PE -phred33^C
  sample_R1.fastq.gz sample_R2.fastq.gz \
  sample_R1_paired.fastq.gz sample_R1_unpaired.fastq.gz \
  sample_R2_paired.fastq.gz sample_R2_unpaired.fastq.gz \
  
(base) tofio17794@cs-929994200285-default:~/bio_info$ ls
'1su5c-RnwFgtee57X6sG5pcHdNsVYsa21?usp=sharing'   LG_BM_MK_PR_001_S35_R1_001.fastq.gz   Miniconda3-latest-Linux-x86_64.sh  'view?usp=drive_link'
(base) tofio17794@cs-929994200285-default:~/bio_info$ trimmomatic -PE -phred33 LG_BM_MK_PR_001_S35_R1_001.fastq.gz sample_trimmed.fastq.gz ILLUMINACLIP:Truseq
3-SE.fa:2:30:10/ LEADING:3/TRAILING:3/ SLIDINGWINDOW:4:15/ MINLEN:36
Usage: 
       PE [-version] [-threads <threads>] [-phred33|-phred64] [-trimlog <trimLogFile>] [-summary <statsSummaryFile>] [-quiet] [-validatePairs] [-basein <inputBase> | <inputFile1> <inputFile2>] [-baseout <outputBase> | <outputFile1P> <outputFile1U> <outputFile2P> <outputFile2U>] <trimmer1>...
   or: 
       SE [-version] [-threads <threads>] [-phred33|-phred64] [-trimlog <trimLogFile>] [-summary <statsSummaryFile>] [-quiet] <inputFile> <outputFile> <trimmer1>...
   or: 
       -version
(base) tofio17794@cs-929994200285-default:~/bio_info$ trimmomatic -SE -phred33 LG_BM_MK_PR_001_S35_R1_001.fastq.gz LG_BM_MK_PR_001_S35_R1_001_trimmed.fastq.gz ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36
Usage: 
       PE [-version] [-threads <threads>] [-phred33|-phred64] [-trimlog <trimLogFile>] [-summary <statsSummaryFile>] [-quiet] [-validatePairs] [-basein <inputBase> | <inputFile1> <inputFile2>] [-baseout <outputBase> | <outputFile1P> <outputFile1U> <outputFile2P> <outputFile2U>] <trimmer1>...
   or: 
       SE [-version] [-threads <threads>] [-phred33|-phred64] [-trimlog <trimLogFile>] [-summary <statsSummaryFile>] [-quiet] <inputFile> <outputFile> <trimmer1>...
   or: 
       -version
(base) tofio17794@cs-929994200285-default:~/bio_info$ trimmomatic SE -phred33 LG_BM_MK_PR_001_S35_R1_001.fastq.gz LG_BM_MK_PR_001_S35_R1_001_trimmed.fastq.gz 
ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36
TrimmomaticSE: Started with arguments:
 -phred33 LG_BM_MK_PR_001_S35_R1_001.fastq.gz LG_BM_MK_PR_001_S35_R1_001_trimmed.fastq.gz ILLUMINACLIP:TruSeq3-SE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36
Automatically using 2 threads
java.io.FileNotFoundException: /home/tofio17794/bio_info/TruSeq3-SE.fa (No such file or directory)
        at java.base/java.io.FileInputStream.open0(Native Method)
        at java.base/java.io.FileInputStream.open(FileInputStream.java:213)
        at java.base/java.io.FileInputStream.<init>(FileInputStream.java:152)
        at org.usadellab.trimmomatic.fasta.FastaParser.parse(FastaParser.java:54)
        at org.usadellab.trimmomatic.trim.IlluminaClippingTrimmer.loadSequences(IlluminaClippingTrimmer.java:110)
        at org.usadellab.trimmomatic.trim.IlluminaClippingTrimmer.makeIlluminaClippingTrimmer(IlluminaClippingTrimmer.java:71)
        at org.usadellab.trimmomatic.trim.TrimmerFactory.makeTrimmer(TrimmerFactory.java:32)
        at org.usadellab.trimmomatic.Trimmomatic.createTrimmers(Trimmomatic.java:59)
        at org.usadellab.trimmomatic.TrimmomaticSE.run(TrimmomaticSE.java:318)
        at org.usadellab.trimmomatic.Trimmomatic.main(Trimmomatic.java:85)
^CTraceback (most recent call last):
  File "/home/tofio17794/miniconda3/bin/trimmomatic", line 103, in <module>
    main()
    ~~~~^^
  File "/home/tofio17794/miniconda3/bin/trimmomatic", line 99, in main
    sys.exit(subprocess.call(java_args))
             ~~~~~~~~~~~~~~~^^^^^^^^^^^
  File "/home/tofio17794/miniconda3/lib/python3.13/subprocess.py", line 399, in call
    return p.wait(timeout=timeout)
           ~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/tofio17794/miniconda3/lib/python3.13/subprocess.py", line 1276, in wait
    return self._wait(timeout=timeout)
           ~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/tofio17794/miniconda3/lib/python3.13/subprocess.py", line 2068, in _wait
    (pid, sts) = self._try_wait(0)
                 ~~~~~~~~~~~~~~^^^
  File "/home/tofio17794/miniconda3/lib/python3.13/subprocess.py", line 2026, in _try_wait
    (pid, sts) = os.waitpid(self.pid, wait_flags)
                 ~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^
KeyboardInterrupt

(base) tofio17794@cs-929994200285-default:~/bio_info$ which TruSeq3-SE.fa
(base) tofio17794@cs-929994200285-default:~/bio_info$ find. -name TruSeq3-SE.fa
-bash: find.: command not found
(base) tofio17794@cs-929994200285-default:~/bio_info$ @
-bash: @: command not found
(base) tofio17794@cs-929994200285-default:~/bio_info$ 
(base) tofio17794@cs-929994200285-default:~/bio_info$ 
(base) tofio17794@cs-929994200285-default:~/bio_info$ 
(base) tofio17794@cs-929994200285-default:~/bio_info$ 
(base) tofio17794@cs-929994200285-default:~/bio_info$ 
(base) tofio17794@cs-929994200285-default:~/bio_info$ 
(base) tofio17794@cs-929994200285-default:~/bio_info$ 
(base) tofio17794@cs-929994200285-default:~/bio_info$ 
(base) tofio17794@cs-929994200285-default:~/bio_info$ find. -name "TruSeq3-SE.fa"
-bash: find.: command not found
(base) tofio17794@cs-929994200285-default:~/bio_info$ find . -name "TruSeq3-SE.fa"
(base) tofio17794@cs-929994200285-default:~/bio_info$ ls ..
bio_info  miniconda3  README-cloudshell.txt
(base) tofio17794@cs-929994200285-default:~/bio_info$ ls ../miniconda3/share/trimmomatic/adapters/
NexteraPE-PE.fa  TruSeq2-PE.fa  TruSeq2-SE.fa  TruSeq3-PE-2.fa  TruSeq3-PE.fa  TruSeq3-SE.fa
(base) tofio17794@cs-929994200285-default:~/bio_info$ cd ..
(base) tofio17794@cs-929994200285-default:~$ find . -name "TruSeq3-SE.fa"
./miniconda3/pkgs/trimmomatic-0.39-hdfd78af_2/share/trimmomatic-0.39-2/adapters/TruSeq3-SE.fa
./miniconda3/share/trimmomatic-0.39-2/adapters/TruSeq3-SE.fa
(base) tofio17794@cs-929994200285-default:~$ ^C
(base) tofio17794@cs-929994200285-default:~$ cd bio_info/
(base) tofio17794@cs-929994200285-default:~/bio_info$ trimmomatic SE -phred33 LG_BM_MK_PR_001_S35_R1_001.fastq.gz LG_BM_MK_PR_001_S35_R1_001_trimmed.fastq.gz ILLUMINACLIP:../miniconda3/share/trimmomatic-0.39-2/adapters/TruSeq3-SE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36
TrimmomaticSE: Started with arguments:
 -phred33 LG_BM_MK_PR_001_S35_R1_001.fastq.gz LG_BM_MK_PR_001_S35_R1_001_trimmed.fastq.gz ILLUMINACLIP:../miniconda3/share/trimmomatic-0.39-2/adapters/TruSeq3-SE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36
Automatically using 2 threads
Using Long Clipping Sequence: 'AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGTA'
Using Long Clipping Sequence: 'AGATCGGAAGAGCACACGTCTGAACTCCAGTCAC'
ILLUMINACLIP: Using 0 prefix pairs, 2 forward/reverse sequences, 0 forward only sequences, 0 reverse only sequences
^CTraceback (most recent call last):
  File "/home/tofio17794/miniconda3/bin/trimmomatic", line 103, in <module>
    main()
    ~~~~^^
  File "/home/tofio17794/miniconda3/bin/trimmomatic", line 99, in main
    sys.exit(subprocess.call(java_args))
             ~~~~~~~~~~~~~~~^^^^^^^^^^^
  File "/home/tofio17794/miniconda3/lib/python3.13/subprocess.py", line 399, in call
    return p.wait(timeout=timeout)
           ~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/tofio17794/miniconda3/lib/python3.13/subprocess.py", line 1276, in wait
    return self._wait(timeout=timeout)
           ~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/tofio17794/miniconda3/lib/python3.13/subprocess.py", line 2068, in _wait
    (pid, sts) = self._try_wait(0)
                 ~~~~~~~~~~~~~~^^^
  File "/home/tofio17794/miniconda3/lib/python3.13/subprocess.py", line 2026, in _try_wait
    (pid, sts) = os.waitpid(self.pid, wait_flags)
                 ~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^
KeyboardInterrupt

(base) tofio17794@cs-929994200285-default:~/bio_info$ trimmomatic SE -phred33 LG_BM_MK_PR_001_S35_R1_001.fastq.gz LG_BM_MK_PR_001_S35_R1_001_trimmed.fastq.gz ILLUMINACLIP:../miniconda3/share/trimmomatic-0.39-2/adapters/TruSeq3-SE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36
TrimmomaticSE: Started with arguments:
 -phred33 LG_BM_MK_PR_001_S35_R1_001.fastq.gz LG_BM_MK_PR_001_S35_R1_001_trimmed.fastq.gz ILLUMINACLIP:../miniconda3/share/trimmomatic-0.39-2/adapters/TruSeq3-SE.fa:2:30:10 LEADING:3 TRAILING:3 SLIDINGWINDOW:4:15 MINLEN:36
Automatically using 2 threads
Using Long Clipping Sequence: 'AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGTA'
Using Long Clipping Sequence: 'AGATCGGAAGAGCACACGTCTGAACTCCAGTCAC'
ILLUMINACLIP: Using 0 prefix pairs, 2 forward/reverse sequences, 0 forward only sequences, 0 reverse only sequences
