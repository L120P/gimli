Some examples using traveltime tomography
Usage: ttinv [options] -p meshfile datafile
Options:    -v (verbose)
            -z zweight (weight for vertical gradients)
            -b/l ubound/lbound (slowness or velocity)
            -R/B (robust and blocky inversion)
            -G initial gradient model

File formats:
    .sgt  (shot-geophone-traveltime) unified data format
    .bms  (binary mesh) GIMLi::Mesh v.1
    .poly (piece-wise linear complex) triangle/tetgen input
            
Refraction seismics

    koenigsee.sgt/.bms  Classical refraction seismics data set
                        with slightly heterogeneous overburden
                        and some high-velocity bedrock
    
@test ttinv -v -z 0.2 -t 8e-4 -p koenigsee.bms koenigsee.sgt @result chi^2 = 0.997091

to view:
	pytripatch -d velocity.vector meshParaDomain.bms


    jmulda-a.sgt/.bms   Joint inversion DC/Ra data set 


