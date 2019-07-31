import pandas as pd
from sas7bdat import SAS7BDAT

input_filename = 'C:\\Users\\Aran\\Downloads\\SASVisualForecasting_sampledatasets\\DCSKINPRODUCT.sas7bdat'
sasb7dat_output_filename = 'C:\\Users\\Aran\\Downloads\\SASVisualForecasting_sampledatasets\\DCSKINPRODUCT.csv'
panda_conv_filename = 'C:\\Users\\Aran\\Downloads\\SASVisualForecasting_sampledatasets\\DCSKINPRODUCT_SAS.csv'

with SAS7BDAT(input_filename, skip_header=True) as reader:
    df = reader.to_data_frame()
    df.to_csv(sasb7dat_output_filename, encoding='utf-8', index_label=None, index=None)

sas_content = pd.read_sas(input_filename)
sas_content.to_csv(panda_conv_filename, encoding='utf-8', index_label=None, index=None)
