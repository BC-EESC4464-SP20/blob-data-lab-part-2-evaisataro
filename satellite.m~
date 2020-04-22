%% 
fn = 'jplMURSST41anommday_6a18_dbf6_f9ec.nc';
%1a. Use the function "ncdisp" to display information about the data contained in this file
%-->
ncdisp(fn)

latt=double(ncread(fn,'latitude'));
long=double(ncread(fn,'longitude'));

t=ncread(fn,'time');
sstAnom=ncread(fn,'sstAnom');
sa_time=datenum(1970,01,01,00,00,t);

Feb_sstAnom=sstAnom(:,:,86);

%%
figure(2); clf
worldmap([20 60],[-170 -100])
contourfm(latt,long, Feb_sstAnom','linecolor','none');
contourcbar
geoshow('landareas.shp','FaceColor','black')
title('Sea Surface Temperature Anomaly from Feb 2020 (^oC)')


