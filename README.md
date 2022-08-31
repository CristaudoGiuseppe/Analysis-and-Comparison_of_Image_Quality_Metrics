# Analysis and Comparison of Image Quality Metrics

<h3>Abstract</h3>

In this essay, the primary objective image quality measures are reviewed. Many image processing applications, including picture restoration, compression, acquisition, enhancement, and others, heavily rely on these metrics. Modern methodologies aim to establish the optimum balance between performance, complexity, and results that are closest to the Human Visual System. This work collects and groups reported quality measures according to their tactics and techniques and proposes a novel method for RGB images.

<h3>Jupyter File</h3>
The jupyter file contains the implementation of the Image Quality Assessments described in the essay as well as the definition and computation of several tests and comparisons between them.

<h3>Dataset</h3>
<b><a href="https://www.ponomarenko.info/tid2008.htm">TID2008</a></b> has been used to evaluate and compare developed IQA. All images in the database are of size 512x384 pixels and different kind of distortions at different levels of intensity have been applied. 

# Libraries

<ul>
    <li>numpy;</li>
    <li>cv2;</li>
    <li>matplotlib;</li>
    <li>skimage;</li>
    <li>pathlib.</li>
</ul>


# Conclusion

Image quality evaluation is critical in a variety of image processing applications. According to the experimental results, MSE and PSNR are very simple, easy to implement, and have low computational complexities. However, these methods do not produce satisfactory results. MSE and PSNR are acceptable image similarity measures only when the images differ by simply increasing a specific type of distortion. When used to measure across distortion types, however, they fail to capture image quality. SSIM is a popular method for measuring image quality. It works well and accurately measures across distortion types better than MSE and PSNR, but fails in the case of a highly blurred image. MS-SSIM is also not very useful for heavily blurred images, but it has a very high prediction rate and is robust when comparing images of different scales. Finally, among the HVS-model-based models, E-SSIM and its extension C-ESSIM produced the worst results. Although I believe it is due to poor implementation, studies show that E-SSIM improves performance by paying more attention to the edges and details in images, which represent the higher layer image structure information.
Better outcomes might be obtained with more fine-tuning of alpha, beta and gamma. Then, the mathematical and HVS-model major goal quality techniques were compared. Results reveal that while HVS-models generally offer greater correlation with subjective measurements, they can sometimes produce subpar results if test pictures suffer from slight degradation (JPEG degradation). Mathematical methods continue to produce accurate and quick findings for the deterioration of Gaussian noise.